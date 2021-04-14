# Hexagonal Architecture - Building blocks

## Interactors

Interactors are use cases. The business logic of your application.
Should be initialized with **Repositories** and **Interactors**.
There are independent of the framework you are using. Should be placed
in the core module of your application.

```java
class ParserInteractor {

    private final StringInputRepository stringInputRepository;
    private final StringEncoderInteractor stringEncoderInteractor;

    public ParserInteractor(
        StringInputRepository stringInputRepository,
        StringEncoderInteractor stringEncoderInteractor
    ) {
        this.stringInputRepository = stringInputRepository;
        this.stringEncoderInteractor = stringEncoderInteractor;
    }

    /**
    * The only public method of interactor. May have any number of arguments
    * Should not have arguments of type 'Repository' or 'Interactor'.
    */
    public String interact(String searchBy) {
        String input = stringInputRepository.find(searchBy);
        String encodedString = stringEncoderInteractor.interact(input);
        return modify(encodedString);
    }

}
```

## Repositories

Repositories are external interfaceses of your application. Repositories
are defined as interfaces in your core module and should be implemented
in application. There may and should depend on the framework you are using.

```java
// In core module

public interface InputStringRepository {

    String find(String searchBy);

}

// Out of core module in your application

public class InputStringRepositoryImpl {

    String find(String searchBy) {
        return resultGotFromDBOrNetwork;
    }

}

```
