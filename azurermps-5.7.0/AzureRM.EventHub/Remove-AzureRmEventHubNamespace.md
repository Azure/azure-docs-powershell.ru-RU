---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732646"
---
# <span data-ttu-id="6d96a-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6d96a-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="6d96a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d96a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d96a-103">Удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="6d96a-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d96a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d96a-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d96a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d96a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d96a-106">Командлет Remove-AzureRmEventHubNamespace удаляет и удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="6d96a-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="6d96a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d96a-107">EXAMPLES</span></span>

### <span data-ttu-id="6d96a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d96a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="6d96a-109">Удаляет пространство имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6d96a-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6d96a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d96a-110">PARAMETERS</span></span>

### <span data-ttu-id="6d96a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d96a-111">-DefaultProfile</span></span>
<span data-ttu-id="6d96a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d96a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d96a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d96a-113">-Name</span></span>
<span data-ttu-id="6d96a-114">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="6d96a-114">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="6d96a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d96a-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d96a-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6d96a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6d96a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d96a-117">-Confirm</span></span>
<span data-ttu-id="6d96a-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d96a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d96a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d96a-119">-WhatIf</span></span>
<span data-ttu-id="6d96a-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d96a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d96a-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d96a-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d96a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d96a-122">CommonParameters</span></span>
<span data-ttu-id="6d96a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d96a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6d96a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d96a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d96a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d96a-125">INPUTS</span></span>

### <span data-ttu-id="6d96a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6d96a-126">System.String</span></span>


## <span data-ttu-id="6d96a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d96a-127">OUTPUTS</span></span>

### <span data-ttu-id="6d96a-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="6d96a-128">System.Object</span></span>

## <span data-ttu-id="6d96a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d96a-129">NOTES</span></span>

## <span data-ttu-id="6d96a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d96a-130">RELATED LINKS</span></span>
