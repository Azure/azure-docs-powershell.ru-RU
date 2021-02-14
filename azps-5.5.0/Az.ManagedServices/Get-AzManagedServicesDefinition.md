---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221548"
---
# <span data-ttu-id="eefcc-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="eefcc-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="eefcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefcc-102">SYNOPSIS</span></span>
<span data-ttu-id="eefcc-103">Получает определенное определение или список определений регистрации.</span><span class="sxs-lookup"><span data-stu-id="eefcc-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="eefcc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eefcc-104">SYNTAX</span></span>

### <span data-ttu-id="eefcc-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eefcc-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eefcc-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="eefcc-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eefcc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eefcc-107">DESCRIPTION</span></span>
<span data-ttu-id="eefcc-108">Получает определенное определение или список определений регистрации.</span><span class="sxs-lookup"><span data-stu-id="eefcc-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="eefcc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eefcc-109">EXAMPLES</span></span>

### <span data-ttu-id="eefcc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eefcc-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="eefcc-111">Получает все определения регистрации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eefcc-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="eefcc-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eefcc-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="eefcc-113">Получает определение регистрации по имени по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eefcc-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="eefcc-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="eefcc-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="eefcc-115">Получает все определения регистрации в заданной области.</span><span class="sxs-lookup"><span data-stu-id="eefcc-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="eefcc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefcc-116">PARAMETERS</span></span>

### <span data-ttu-id="eefcc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefcc-117">-DefaultProfile</span></span>
<span data-ttu-id="eefcc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eefcc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eefcc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eefcc-119">-Name</span></span>
<span data-ttu-id="eefcc-120">Уникальное имя определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="eefcc-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="eefcc-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="eefcc-121">-Scope</span></span>
<span data-ttu-id="eefcc-122">Область создания определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="eefcc-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="eefcc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefcc-123">CommonParameters</span></span>
<span data-ttu-id="eefcc-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefcc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefcc-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eefcc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefcc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eefcc-126">INPUTS</span></span>

### <span data-ttu-id="eefcc-127">Нет</span><span class="sxs-lookup"><span data-stu-id="eefcc-127">None</span></span>
## <span data-ttu-id="eefcc-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eefcc-128">OUTPUTS</span></span>

### <span data-ttu-id="eefcc-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="eefcc-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="eefcc-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eefcc-130">NOTES</span></span>

## <span data-ttu-id="eefcc-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eefcc-131">RELATED LINKS</span></span>
