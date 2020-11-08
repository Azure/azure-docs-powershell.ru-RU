---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247336"
---
# <span data-ttu-id="9e21a-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9e21a-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="9e21a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e21a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e21a-103">Возвращает определенную регистрационную запись или список определений регистрации.</span><span class="sxs-lookup"><span data-stu-id="9e21a-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="9e21a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e21a-104">SYNTAX</span></span>

### <span data-ttu-id="9e21a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e21a-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e21a-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="9e21a-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e21a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e21a-107">DESCRIPTION</span></span>
<span data-ttu-id="9e21a-108">Возвращает определенную регистрационную запись или список определений регистрации.</span><span class="sxs-lookup"><span data-stu-id="9e21a-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="9e21a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e21a-109">EXAMPLES</span></span>

### <span data-ttu-id="9e21a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e21a-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="9e21a-111">Получает определения всех регистраций в области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e21a-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="9e21a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9e21a-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="9e21a-113">Получает определение регистрации по имени в области по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e21a-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="9e21a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9e21a-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="9e21a-115">Получает все определения регистрации в заданной области.</span><span class="sxs-lookup"><span data-stu-id="9e21a-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="9e21a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e21a-116">PARAMETERS</span></span>

### <span data-ttu-id="9e21a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e21a-117">-DefaultProfile</span></span>
<span data-ttu-id="9e21a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e21a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e21a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e21a-119">-Name</span></span>
<span data-ttu-id="9e21a-120">Уникальное имя определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="9e21a-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="9e21a-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="9e21a-121">-Scope</span></span>
<span data-ttu-id="9e21a-122">Область, в которой создано определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="9e21a-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="9e21a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e21a-123">CommonParameters</span></span>
<span data-ttu-id="9e21a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e21a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e21a-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e21a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e21a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e21a-126">INPUTS</span></span>

### <span data-ttu-id="9e21a-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="9e21a-127">None</span></span>
## <span data-ttu-id="9e21a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e21a-128">OUTPUTS</span></span>

### <span data-ttu-id="9e21a-129">Microsoft. Azure. PowerShell. командлеты. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="9e21a-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="9e21a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e21a-130">NOTES</span></span>

## <span data-ttu-id="9e21a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e21a-131">RELATED LINKS</span></span>
