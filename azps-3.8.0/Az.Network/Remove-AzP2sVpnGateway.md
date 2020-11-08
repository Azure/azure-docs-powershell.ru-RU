---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074060"
---
# <span data-ttu-id="88d2f-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="88d2f-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="88d2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="88d2f-103">Удаление существующего P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="88d2f-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="88d2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88d2f-104">SYNTAX</span></span>

### <span data-ttu-id="88d2f-105">ByP2SVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88d2f-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88d2f-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="88d2f-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88d2f-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="88d2f-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88d2f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88d2f-108">DESCRIPTION</span></span>
<span data-ttu-id="88d2f-109">Командлет **Remove-AzP2sVpnGateway** позволяет удалить существующий P2SVpnGateway в разделе VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="88d2f-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="88d2f-110">После удаления P2SVpnGateway все клиенты, которые указывают на возможности подключения клиентов сайта, будут завершаться сбоем.</span><span class="sxs-lookup"><span data-stu-id="88d2f-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="88d2f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88d2f-111">EXAMPLES</span></span>

### <span data-ttu-id="88d2f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88d2f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="88d2f-113">Командлет **Remove-AzP2sVpnGateway** позволяет удалить существующий P2SVpnGateway в разделе VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="88d2f-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="88d2f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88d2f-114">PARAMETERS</span></span>

### <span data-ttu-id="88d2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d2f-115">-DefaultProfile</span></span>
<span data-ttu-id="88d2f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88d2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d2f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="88d2f-117">-Force</span></span>
<span data-ttu-id="88d2f-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="88d2f-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88d2f-119">-InputObject</span></span>
<span data-ttu-id="88d2f-120">Объект p2sVpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="88d2f-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88d2f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88d2f-121">-Name</span></span>
<span data-ttu-id="88d2f-122">Имя P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="88d2f-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d2f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88d2f-123">-PassThru</span></span>
<span data-ttu-id="88d2f-124">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="88d2f-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d2f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88d2f-125">-ResourceGroupName</span></span>
<span data-ttu-id="88d2f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88d2f-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d2f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88d2f-127">-ResourceId</span></span>
<span data-ttu-id="88d2f-128">Идентификатор ресурса Azure для p2sVpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="88d2f-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88d2f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88d2f-129">-Confirm</span></span>
<span data-ttu-id="88d2f-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88d2f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d2f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d2f-131">-WhatIf</span></span>
<span data-ttu-id="88d2f-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88d2f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d2f-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88d2f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d2f-134">CommonParameters</span></span>
<span data-ttu-id="88d2f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88d2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d2f-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d2f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d2f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88d2f-137">INPUTS</span></span>

### <span data-ttu-id="88d2f-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="88d2f-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="88d2f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="88d2f-139">System.String</span></span>

## <span data-ttu-id="88d2f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88d2f-140">OUTPUTS</span></span>

### <span data-ttu-id="88d2f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88d2f-141">System.Boolean</span></span>

## <span data-ttu-id="88d2f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="88d2f-142">NOTES</span></span>

## <span data-ttu-id="88d2f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88d2f-143">RELATED LINKS</span></span>
