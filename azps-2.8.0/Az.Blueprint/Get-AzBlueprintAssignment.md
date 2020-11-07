---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 121811c88493a4f6f069a60c8f9662eb9d11303e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727641"
---
# <span data-ttu-id="3076f-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3076f-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="3076f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3076f-102">SYNOPSIS</span></span>
<span data-ttu-id="3076f-103">Получение одного или нескольких назначений для чертежей.</span><span class="sxs-lookup"><span data-stu-id="3076f-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="3076f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3076f-104">SYNTAX</span></span>

### <span data-ttu-id="3076f-105">BlueprintAssignmentsBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3076f-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3076f-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="3076f-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3076f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3076f-107">DESCRIPTION</span></span>
<span data-ttu-id="3076f-108">Получение одного или нескольких назначений для чертежей.</span><span class="sxs-lookup"><span data-stu-id="3076f-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="3076f-109">В области подписок существуют назначения для планов.</span><span class="sxs-lookup"><span data-stu-id="3076f-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="3076f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3076f-110">EXAMPLES</span></span>

### <span data-ttu-id="3076f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3076f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="3076f-112">Получение назначений в заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="3076f-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="3076f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3076f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="3076f-114">Получение задания из плана с заданным именем в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="3076f-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="3076f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3076f-115">PARAMETERS</span></span>

### <span data-ttu-id="3076f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3076f-116">-DefaultProfile</span></span>
<span data-ttu-id="3076f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3076f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3076f-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3076f-118">-Name</span></span>
<span data-ttu-id="3076f-119">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="3076f-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3076f-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3076f-120">-SubscriptionId</span></span>
<span data-ttu-id="3076f-121">Идентификатор подписки, на которую развертывается назначение.</span><span class="sxs-lookup"><span data-stu-id="3076f-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3076f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3076f-122">CommonParameters</span></span>
<span data-ttu-id="3076f-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3076f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3076f-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3076f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3076f-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3076f-125">INPUTS</span></span>

### <span data-ttu-id="3076f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3076f-126">System.String</span></span>

## <span data-ttu-id="3076f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3076f-127">OUTPUTS</span></span>

### <span data-ttu-id="3076f-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="3076f-128">System.Object</span></span>
## <span data-ttu-id="3076f-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3076f-129">NOTES</span></span>

## <span data-ttu-id="3076f-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3076f-130">RELATED LINKS</span></span>
