---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236577"
---
# <span data-ttu-id="53a25-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="53a25-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="53a25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a25-102">SYNOPSIS</span></span>
<span data-ttu-id="53a25-103">Удаляет существующий P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="53a25-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="53a25-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53a25-104">SYNTAX</span></span>

### <span data-ttu-id="53a25-105">ByP2SVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53a25-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a25-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="53a25-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a25-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="53a25-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a25-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53a25-108">DESCRIPTION</span></span>
<span data-ttu-id="53a25-109">С помощью cmdlet **Remove-AzP2sVpnGateway** можно удалить существующий проект P2SVpnGateway в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="53a25-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="53a25-110">При удалении P2SVpnGateway соединение с клиентами сайтов будет сбой.</span><span class="sxs-lookup"><span data-stu-id="53a25-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="53a25-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53a25-111">EXAMPLES</span></span>

### <span data-ttu-id="53a25-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53a25-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="53a25-113">С помощью cmdlet **Remove-AzP2sVpnGateway** можно удалить существующий проект P2SVpnGateway в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="53a25-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="53a25-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53a25-114">PARAMETERS</span></span>

### <span data-ttu-id="53a25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a25-115">-DefaultProfile</span></span>
<span data-ttu-id="53a25-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53a25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a25-117">-Force</span><span class="sxs-lookup"><span data-stu-id="53a25-117">-Force</span></span>
<span data-ttu-id="53a25-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="53a25-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="53a25-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53a25-119">-InputObject</span></span>
<span data-ttu-id="53a25-120">Объект p2sVpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="53a25-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="53a25-121">-Name</span><span class="sxs-lookup"><span data-stu-id="53a25-121">-Name</span></span>
<span data-ttu-id="53a25-122">Имя P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="53a25-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="53a25-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53a25-123">-PassThru</span></span>
<span data-ttu-id="53a25-124">Возвращает объект, представляющий элемент, для которого выполняется эта операция.</span><span class="sxs-lookup"><span data-stu-id="53a25-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="53a25-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a25-125">-ResourceGroupName</span></span>
<span data-ttu-id="53a25-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53a25-126">The resource group name.</span></span>

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

### <span data-ttu-id="53a25-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53a25-127">-ResourceId</span></span>
<span data-ttu-id="53a25-128">ИД ресурса Azure для p2sVpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="53a25-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="53a25-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53a25-129">-Confirm</span></span>
<span data-ttu-id="53a25-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a25-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a25-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a25-131">-WhatIf</span></span>
<span data-ttu-id="53a25-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a25-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a25-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53a25-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a25-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a25-134">CommonParameters</span></span>
<span data-ttu-id="53a25-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a25-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a25-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a25-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a25-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53a25-137">INPUTS</span></span>

### <span data-ttu-id="53a25-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="53a25-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="53a25-139">System.String</span><span class="sxs-lookup"><span data-stu-id="53a25-139">System.String</span></span>

## <span data-ttu-id="53a25-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53a25-140">OUTPUTS</span></span>

### <span data-ttu-id="53a25-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="53a25-141">System.Boolean</span></span>

## <span data-ttu-id="53a25-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53a25-142">NOTES</span></span>

## <span data-ttu-id="53a25-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53a25-143">RELATED LINKS</span></span>
