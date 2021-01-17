---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400159"
---
# <span data-ttu-id="2c691-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="2c691-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="2c691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c691-102">SYNOPSIS</span></span>
<span data-ttu-id="2c691-103">Возвращает определенное назначение или список заданий по регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="2c691-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c691-104">SYNTAX</span></span>

### <span data-ttu-id="2c691-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c691-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c691-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2c691-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c691-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c691-107">DESCRIPTION</span></span>
<span data-ttu-id="2c691-108">Возвращает определенное назначение или список заданий по регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="2c691-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c691-109">EXAMPLES</span></span>

### <span data-ttu-id="2c691-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c691-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="2c691-111">Получает все назначения регистрации, которые находятся в области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c691-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="2c691-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2c691-112">Example 2</span></span>
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

<span data-ttu-id="2c691-113">Получает все назначения по регистрации с подробными сведениями об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="2c691-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2c691-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="2c691-115">Получает назначение регистрации по имени без сведений об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="2c691-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="2c691-116">Example 4</span></span>
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

<span data-ttu-id="2c691-117">Получает назначение регистрации по имени со сведениями об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="2c691-118">Пример 5</span><span class="sxs-lookup"><span data-stu-id="2c691-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="2c691-119">Получает все назначения регистрации в заданной области.</span><span class="sxs-lookup"><span data-stu-id="2c691-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="2c691-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c691-120">PARAMETERS</span></span>

### <span data-ttu-id="2c691-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c691-121">-DefaultProfile</span></span>
<span data-ttu-id="2c691-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c691-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c691-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="2c691-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="2c691-124">Следует ли включать сведения об определении регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="2c691-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2c691-125">-Name</span></span>
<span data-ttu-id="2c691-126">Уникальное имя задания регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="2c691-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="2c691-127">-Scope</span></span>
<span data-ttu-id="2c691-128">Область создания назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="2c691-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="2c691-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c691-129">CommonParameters</span></span>
<span data-ttu-id="2c691-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c691-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c691-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c691-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c691-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c691-132">INPUTS</span></span>

### <span data-ttu-id="2c691-133">Нет</span><span class="sxs-lookup"><span data-stu-id="2c691-133">None</span></span>
## <span data-ttu-id="2c691-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c691-134">OUTPUTS</span></span>

### <span data-ttu-id="2c691-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="2c691-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="2c691-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c691-136">NOTES</span></span>

## <span data-ttu-id="2c691-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c691-137">RELATED LINKS</span></span>
