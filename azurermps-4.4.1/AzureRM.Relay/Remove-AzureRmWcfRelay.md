---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569235"
---
# <span data-ttu-id="b8edb-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="b8edb-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="b8edb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8edb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8edb-103">Удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="b8edb-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8edb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8edb-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8edb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8edb-105">DESCRIPTION</span></span>
<span data-ttu-id="b8edb-106">Командлет **Remove-AzureRmWcfRelay** удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="b8edb-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="b8edb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8edb-107">EXAMPLES</span></span>

### <span data-ttu-id="b8edb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8edb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="b8edb-109">Удаляет WcfRelay `TestWCFRelay1` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b8edb-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="b8edb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8edb-110">PARAMETERS</span></span>

### <span data-ttu-id="b8edb-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8edb-111">-Namespace</span></span>
<span data-ttu-id="b8edb-112">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b8edb-112">Namespace Name.</span></span>

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

### <span data-ttu-id="b8edb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8edb-113">-ResourceGroupName</span></span>
<span data-ttu-id="b8edb-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8edb-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="b8edb-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8edb-115">-Name</span></span>
<span data-ttu-id="b8edb-116">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="b8edb-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b8edb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8edb-117">-Confirm</span></span>
<span data-ttu-id="b8edb-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8edb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8edb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8edb-119">-WhatIf</span></span>
<span data-ttu-id="b8edb-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8edb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8edb-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8edb-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8edb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8edb-122">-DefaultProfile</span></span>
<span data-ttu-id="b8edb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8edb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8edb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8edb-124">CommonParameters</span></span>
<span data-ttu-id="b8edb-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8edb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8edb-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8edb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8edb-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8edb-127">INPUTS</span></span>

### <span data-ttu-id="b8edb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8edb-128">-ResourceGroupName</span></span>
 <span data-ttu-id="b8edb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b8edb-129">System.String</span></span>
 

### <span data-ttu-id="b8edb-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8edb-130">-Namespace</span></span>
 <span data-ttu-id="b8edb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b8edb-131">System.String</span></span>
 

### <span data-ttu-id="b8edb-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8edb-132">-Name</span></span>
 <span data-ttu-id="b8edb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b8edb-133">System.String</span></span>

## <span data-ttu-id="b8edb-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8edb-134">OUTPUTS</span></span>

### <span data-ttu-id="b8edb-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="b8edb-135">System.Object</span></span>

## <span data-ttu-id="b8edb-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8edb-136">NOTES</span></span>

## <span data-ttu-id="b8edb-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8edb-137">RELATED LINKS</span></span>

