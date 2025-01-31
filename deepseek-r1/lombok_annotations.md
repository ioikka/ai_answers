# Lombok Annotations Categorized by Use Cases

## 1. Data Handling

- `@Data`  
  Combines `@ToString`, `@EqualsAndHashCode`, `@Getter`, `@Setter`, and `@RequiredArgsConstructor` for POJOs.

- `@Getter` / `@Setter`  
  Generates getter/setter methods for fields.

- `@Value`  
  Creates an immutable class (like `@Data` but with final fields, no setters, and all-args constructor).

- `@With`  
  Generates a clone method to create a new object with a single field changed (useful for immutability).

## 2. Constructor Generation

- `@NoArgsConstructor`  
  Generates a no-argument constructor.

- `@AllArgsConstructor`  
  Generates a constructor with all fields as arguments.

- `@RequiredArgsConstructor`  
  Creates a constructor for final or `@NonNull` fields.

## 3. Builder Pattern

- `@Builder`  
  Implements the Builder pattern for object creation.

- `@Singular`  
  Adds "add" methods for collections in builders (e.g., `List<String> names → .name("Alice")`).

- `@Builder.Default`  
  Specifies default values for builder-created objects.

## 4. Logging

- `@Slf4j`  
  Injects a log field for SLF4J logging.

- `@Log`, `@Log4j`, `@Log4j2`, `@CommonsLog`, `@JBossLog`  
  Injects loggers for other frameworks (e.g., Java Util Logging, Apache Commons, etc.).

## 5. Utility Methods

- `@ToString`  
  Generates a `toString()` method.

- `@EqualsAndHashCode`  
  Generates `equals()` and `hashCode()` methods based on fields.

- `@NonNull`  
  Adds null checks on parameters (e.g., in setters or constructors).

## 6. Resource Management

- `@Cleanup`  
  Automatically closes resources (e.g., `InputStream`, `OutputStream`) using try-with-resources.

## 7. Delegation

- `@Delegate`  
  Delegates method calls from a field to the enclosing class (e.g., for composition over inheritance).

## 8. Synchronization

- `@Synchronized`  
  Generates a synchronized block around a method.

## 9. Exception Handling

- `@SneakyThrows`  
  Silently throws checked exceptions without declaring them (use with caution!).

## 10. Experimental Features

- `@Accessors`  
  Customizes getter/setter names (e.g., `@Accessors(fluent = true)` for method chaining).

- `@SuperBuilder`  
  Enables builders for classes with superclasses.

- `@FieldDefaults`  
  Adds access modifiers (e.g., `private final`) to all fields.

- `@UtilityClass`  
  Marks a class as a utility class (private constructor, static methods).

## 11. Configuration

- `@FieldNameConstants`  
  Generates constants for field names (e.g., `Fields.NAME` for a field name).

## When to Use Experimental Annotations

Experimental features (e.g., `@SuperBuilder`, `@UtilityClass`) require adding `lombok.experimental` to your imports and may change in future releases.

This grouping helps streamline code generation for common patterns like POJOs, builders, logging, and immutability while reducing boilerplate. Always check the Lombok documentation for updates!
