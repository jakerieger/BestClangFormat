# Best Clang Format

### Example
```cpp
#include "string"

#define NEXT_NUMBER(PARAM) ((PARAM) + 1)

int globalVariable;

//Single line comment
typedef enum Kinds {
    /* Block comment */
    EnumeratorA,
    EnumeratorB
} KindsTypedef;

/**
 * \brief Doxygen comment 
 */
struct StructType {
    void structMember();
    int structDataMember;

    friend bool operator==(const StructType& lhs, const StructType& rhs);
};

namespace namespace_name {
    template<class>
    concept bool Test = true;

    template<typename TypeParameter>
    class ClassType {
        void classMember() {
            TypeParameter.DependentName();
        }

        static void staticClassMember();
        int classDataMember;
        static int staticClassDataMember;
    };

    union UnionType {
        StructType unionMember1;
        ClassType<StructType> unionMember2;
    };

    std::string globalFunction(StructType paramA, StructType paramB) {
        auto localNumber   = 123456 + 123456.f + '!';
        auto localVariable = "String" R"(RawString)";
        if (paramA == paramB)
            return localVariable;
    }
}

UCLASS(Abstract,
       ClassGroup = Environment,
       meta       = (Tooltip = "Very important tooltip"))

class MYGAME_API AAtmosphere : public AActor {
    GENERATED_BODY()
};

```