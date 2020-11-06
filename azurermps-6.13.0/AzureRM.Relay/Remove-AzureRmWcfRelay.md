---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 5e49497f8784e9686c84cb75dde4b8fd4297578d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562723"
---
# <span data-ttu-id="88aac-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="88aac-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="88aac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88aac-102">SYNOPSIS</span></span>
<span data-ttu-id="88aac-103">Удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="88aac-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88aac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88aac-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88aac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88aac-105">DESCRIPTION</span></span>
<span data-ttu-id="88aac-106">Командлет **Remove-AzureRmWcfRelay** удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="88aac-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="88aac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88aac-107">EXAMPLES</span></span>

### <span data-ttu-id="88aac-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88aac-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="88aac-109">Удаляет WcfRelay `TestWCFRelay1` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="88aac-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="88aac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88aac-110">PARAMETERS</span></span>

### <span data-ttu-id="88aac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88aac-111">-DefaultProfile</span></span>
<span data-ttu-id="88aac-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88aac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88aac-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88aac-113">-Name</span></span>
<span data-ttu-id="88aac-114">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="88aac-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88aac-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="88aac-115">-Namespace</span></span>
<span data-ttu-id="88aac-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="88aac-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88aac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88aac-117">-ResourceGroupName</span></span>
<span data-ttu-id="88aac-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88aac-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88aac-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88aac-119">-Confirm</span></span>
<span data-ttu-id="88aac-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88aac-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88aac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88aac-121">-WhatIf</span></span>
<span data-ttu-id="88aac-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88aac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88aac-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88aac-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88aac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88aac-124">CommonParameters</span></span>
<span data-ttu-id="88aac-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88aac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="88aac-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88aac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88aac-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88aac-127">INPUTS</span></span>

### <span data-ttu-id="88aac-128">System. String</span><span class="sxs-lookup"><span data-stu-id="88aac-128">System.String</span></span>


## <span data-ttu-id="88aac-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88aac-129">OUTPUTS</span></span>

### <span data-ttu-id="88aac-130">System. void</span><span class="sxs-lookup"><span data-stu-id="88aac-130">System.Void</span></span>


## <span data-ttu-id="88aac-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="88aac-131">NOTES</span></span>

## <span data-ttu-id="88aac-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88aac-132">RELATED LINKS</span></span>
