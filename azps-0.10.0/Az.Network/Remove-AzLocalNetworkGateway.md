---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 0589fa3f5dd806149c243557b547455af35178b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909474"
---
# <span data-ttu-id="52702-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52702-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="52702-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52702-102">SYNOPSIS</span></span>
<span data-ttu-id="52702-103">Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="52702-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="52702-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52702-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52702-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52702-105">DESCRIPTION</span></span>
<span data-ttu-id="52702-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="52702-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="52702-107">Командлет **Remove-AzLocalNetworkGateway** удаляет объект, представляющий локальный шлюз, на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52702-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="52702-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52702-108">EXAMPLES</span></span>

### <span data-ttu-id="52702-109">1: Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="52702-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="52702-110">Удаляет объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="52702-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="52702-111">Примечание. необходимо сначала удалить все подключения к шлюзу локальной сети с помощью командлета **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="52702-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="52702-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52702-112">PARAMETERS</span></span>

### <span data-ttu-id="52702-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52702-113">-AsJob</span></span>
<span data-ttu-id="52702-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="52702-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52702-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52702-115">-DefaultProfile</span></span>
<span data-ttu-id="52702-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52702-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52702-117">-Force</span><span class="sxs-lookup"><span data-stu-id="52702-117">-Force</span></span>
<span data-ttu-id="52702-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="52702-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52702-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52702-119">-Name</span></span>
<span data-ttu-id="52702-120">Указывает имя шлюза локальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="52702-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52702-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52702-121">-PassThru</span></span>
<span data-ttu-id="52702-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="52702-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52702-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="52702-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52702-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52702-124">-ResourceGroupName</span></span>
<span data-ttu-id="52702-125">Указывает имя группы ресурсов, которая содержит шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="52702-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52702-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52702-126">-Confirm</span></span>
<span data-ttu-id="52702-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52702-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52702-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52702-128">-WhatIf</span></span>
<span data-ttu-id="52702-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52702-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52702-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52702-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52702-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52702-131">CommonParameters</span></span>
<span data-ttu-id="52702-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52702-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52702-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52702-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52702-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52702-134">INPUTS</span></span>

## <span data-ttu-id="52702-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52702-135">OUTPUTS</span></span>

## <span data-ttu-id="52702-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="52702-136">NOTES</span></span>

## <span data-ttu-id="52702-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52702-137">RELATED LINKS</span></span>

[<span data-ttu-id="52702-138">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52702-138">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="52702-139">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52702-139">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="52702-140">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52702-140">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)


