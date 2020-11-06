---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563535"
---
# <span data-ttu-id="5c086-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="5c086-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="5c086-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c086-102">SYNOPSIS</span></span>
<span data-ttu-id="5c086-103">Получение сведений об одном концентраторе событий или получение списка концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="5c086-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c086-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c086-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c086-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c086-105">DESCRIPTION</span></span>
<span data-ttu-id="5c086-106">Командлет Get-AzureRmEventHub возвращает либо сведения о концентраторе событий, либо список всех концентраторов событий в текущем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5c086-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="5c086-107">Если указано имя концентратора событий, возвращаются сведения об одном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="5c086-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="5c086-108">Если имя концентратора событий не указано, возвращается список всех концентраторов событий в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5c086-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="5c086-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c086-109">EXAMPLES</span></span>

### <span data-ttu-id="5c086-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c086-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="5c086-111">Возвращает сведения о концентраторе событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="5c086-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="5c086-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5c086-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="5c086-113">Возвращает список концентраторов событий в MyNamespaceName пространства имен \` \` .</span><span class="sxs-lookup"><span data-stu-id="5c086-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="5c086-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c086-114">PARAMETERS</span></span>

### <span data-ttu-id="5c086-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c086-115">-DefaultProfile</span></span>
<span data-ttu-id="5c086-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c086-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c086-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c086-117">-Name</span></span>
<span data-ttu-id="5c086-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="5c086-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c086-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c086-119">-Namespace</span></span>
<span data-ttu-id="5c086-120">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="5c086-120">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c086-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c086-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c086-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5c086-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c086-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c086-123">CommonParameters</span></span>
<span data-ttu-id="5c086-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c086-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5c086-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c086-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c086-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c086-126">INPUTS</span></span>

### <span data-ttu-id="5c086-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5c086-127">System.String</span></span>


## <span data-ttu-id="5c086-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c086-128">OUTPUTS</span></span>

### <span data-ttu-id="5c086-129">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.5.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="5c086-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="5c086-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c086-130">NOTES</span></span>

## <span data-ttu-id="5c086-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c086-131">RELATED LINKS</span></span>
