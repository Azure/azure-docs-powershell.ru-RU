---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506249"
---
# <span data-ttu-id="83fa4-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="83fa4-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="83fa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="83fa4-103">Возвращает определенное назначение или список заданий по регистрации.</span><span class="sxs-lookup"><span data-stu-id="83fa4-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="83fa4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83fa4-104">SYNTAX</span></span>

### <span data-ttu-id="83fa4-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83fa4-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83fa4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="83fa4-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83fa4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83fa4-107">DESCRIPTION</span></span>
<span data-ttu-id="83fa4-108">Возвращает определенное назначение или список заданий по регистрации.</span><span class="sxs-lookup"><span data-stu-id="83fa4-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="83fa4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83fa4-109">EXAMPLES</span></span>

### <span data-ttu-id="83fa4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83fa4-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="83fa4-111">Получает все назначения регистрации, которые находятся в области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83fa4-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="83fa4-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="83fa4-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="83fa4-113">Получает все назначения по регистрации с подробными сведениями об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="83fa4-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="83fa4-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="83fa4-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="83fa4-115">Получает назначение регистрации по имени без сведений об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="83fa4-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="83fa4-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="83fa4-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="83fa4-117">Получает назначение регистрации по имени с подробными сведениями об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="83fa4-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="83fa4-118">Пример 5</span><span class="sxs-lookup"><span data-stu-id="83fa4-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="83fa4-119">Получает все назначения регистрации в заданной области.</span><span class="sxs-lookup"><span data-stu-id="83fa4-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="83fa4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83fa4-120">PARAMETERS</span></span>

### <span data-ttu-id="83fa4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fa4-121">-DefaultProfile</span></span>
<span data-ttu-id="83fa4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83fa4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fa4-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="83fa4-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="83fa4-124">Следует ли включать сведения об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="83fa4-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fa4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="83fa4-125">-Name</span></span>
<span data-ttu-id="83fa4-126">Уникальное имя регистрационного назначения.</span><span class="sxs-lookup"><span data-stu-id="83fa4-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fa4-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="83fa4-127">-Scope</span></span>
<span data-ttu-id="83fa4-128">Область создания назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="83fa4-128">The scope where the registration assignment created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fa4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fa4-129">CommonParameters</span></span>
<span data-ttu-id="83fa4-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83fa4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fa4-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83fa4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fa4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83fa4-132">INPUTS</span></span>

### <span data-ttu-id="83fa4-133">Нет</span><span class="sxs-lookup"><span data-stu-id="83fa4-133">None</span></span>
## <span data-ttu-id="83fa4-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83fa4-134">OUTPUTS</span></span>

### <span data-ttu-id="83fa4-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="83fa4-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="83fa4-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83fa4-136">NOTES</span></span>

## <span data-ttu-id="83fa4-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83fa4-137">RELATED LINKS</span></span>
