---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: d65e19cb86a2ba850311fa937e64432ee8588d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567994"
---
# <span data-ttu-id="4765f-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4765f-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="4765f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4765f-102">SYNOPSIS</span></span>
<span data-ttu-id="4765f-103">Получает сведения о пространстве имен концентраторов событий или получает список всех пространств имен концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="4765f-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4765f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4765f-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4765f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4765f-105">DESCRIPTION</span></span>
<span data-ttu-id="4765f-106">Командлет Get-AzureRmEventHubNamespace получает либо сведения о заданном пространстве имен концентраторов событий, либо список всех пространств имен концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="4765f-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="4765f-107">Если указано имя пространства имен, возвращается информация об одном пространстве имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="4765f-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="4765f-108">Если имя пространства имен не указано, возвращается список пространств имен.</span><span class="sxs-lookup"><span data-stu-id="4765f-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="4765f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4765f-109">EXAMPLES</span></span>

### <span data-ttu-id="4765f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4765f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="4765f-111">Получает сведения о пространстве имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4765f-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4765f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4765f-112">PARAMETERS</span></span>

### <span data-ttu-id="4765f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4765f-113">-DefaultProfile</span></span>
<span data-ttu-id="4765f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4765f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4765f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4765f-115">-Name</span></span>
<span data-ttu-id="4765f-116">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="4765f-116">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4765f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4765f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4765f-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4765f-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4765f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4765f-119">CommonParameters</span></span>
<span data-ttu-id="4765f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4765f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4765f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4765f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4765f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4765f-122">INPUTS</span></span>

### <span data-ttu-id="4765f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4765f-123">System.String</span></span>


## <span data-ttu-id="4765f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4765f-124">OUTPUTS</span></span>

### <span data-ttu-id="4765f-125">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.5.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4765f-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="4765f-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4765f-126">NOTES</span></span>

## <span data-ttu-id="4765f-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4765f-127">RELATED LINKS</span></span>
