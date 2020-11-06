---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 02949f3a16c9a259e645a035ce3e762db9582024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561575"
---
# <span data-ttu-id="764c8-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="764c8-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="764c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="764c8-102">SYNOPSIS</span></span>
<span data-ttu-id="764c8-103">Удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="764c8-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="764c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="764c8-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="764c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="764c8-105">DESCRIPTION</span></span>
<span data-ttu-id="764c8-106">Командлет **Remove-AzureRmWcfRelay** удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="764c8-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="764c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="764c8-107">EXAMPLES</span></span>

### <span data-ttu-id="764c8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="764c8-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="764c8-109">Удаляет WcfRelay `TestWCFRelay1` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="764c8-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="764c8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="764c8-110">PARAMETERS</span></span>

### <span data-ttu-id="764c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="764c8-111">-DefaultProfile</span></span>
<span data-ttu-id="764c8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="764c8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="764c8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="764c8-113">-Name</span></span>
<span data-ttu-id="764c8-114">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="764c8-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="764c8-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="764c8-115">-Namespace</span></span>
<span data-ttu-id="764c8-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="764c8-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="764c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="764c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="764c8-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="764c8-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="764c8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="764c8-119">-Confirm</span></span>
<span data-ttu-id="764c8-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="764c8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764c8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="764c8-121">-WhatIf</span></span>
<span data-ttu-id="764c8-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="764c8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="764c8-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="764c8-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764c8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764c8-124">CommonParameters</span></span>
<span data-ttu-id="764c8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="764c8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764c8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764c8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764c8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="764c8-127">INPUTS</span></span>

### <span data-ttu-id="764c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="764c8-128">-ResourceGroupName</span></span>
 <span data-ttu-id="764c8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="764c8-129">System.String</span></span>
 

### <span data-ttu-id="764c8-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="764c8-130">-Namespace</span></span>
 <span data-ttu-id="764c8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="764c8-131">System.String</span></span>
 

### <span data-ttu-id="764c8-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="764c8-132">-Name</span></span>
 <span data-ttu-id="764c8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="764c8-133">System.String</span></span>

## <span data-ttu-id="764c8-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="764c8-134">OUTPUTS</span></span>

### <span data-ttu-id="764c8-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="764c8-135">System.Object</span></span>

## <span data-ttu-id="764c8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="764c8-136">NOTES</span></span>

## <span data-ttu-id="764c8-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="764c8-137">RELATED LINKS</span></span>

