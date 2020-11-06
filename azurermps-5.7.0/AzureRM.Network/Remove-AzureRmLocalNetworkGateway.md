---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 1aca9335da67bb3c1144f67fb8f14ad9b2a7f1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558999"
---
# <span data-ttu-id="b4ce4-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4ce4-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="b4ce4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ce4-103">Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="b4ce4-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4ce4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4ce4-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ce4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ce4-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="b4ce4-107">Командлет **Remove-AzureRmLocalNetworkGateway** удаляет объект, представляющий локальный шлюз, на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b4ce4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4ce4-108">EXAMPLES</span></span>

### <span data-ttu-id="b4ce4-109">1: Удаление шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="b4ce4-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="b4ce4-110">Удаляет объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="b4ce4-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="b4ce4-111">Примечание. необходимо сначала удалить все подключения к шлюзу локальной сети с помощью командлета **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="b4ce4-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="b4ce4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4ce4-112">PARAMETERS</span></span>

### <span data-ttu-id="b4ce4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ce4-113">-AsJob</span></span>
<span data-ttu-id="b4ce4-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b4ce4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4ce4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ce4-115">-DefaultProfile</span></span>
<span data-ttu-id="b4ce4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ce4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b4ce4-117">-Force</span></span>
<span data-ttu-id="b4ce4-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4ce4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4ce4-119">-Name</span></span>
<span data-ttu-id="b4ce4-120">Указывает имя шлюза локальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b4ce4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ce4-121">-PassThru</span></span>
<span data-ttu-id="b4ce4-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4ce4-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4ce4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ce4-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4ce4-125">Указывает имя группы ресурсов, которая содержит шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="b4ce4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4ce4-126">-Confirm</span></span>
<span data-ttu-id="b4ce4-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ce4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ce4-128">-WhatIf</span></span>
<span data-ttu-id="b4ce4-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ce4-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ce4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ce4-131">CommonParameters</span></span>
<span data-ttu-id="b4ce4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ce4-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ce4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ce4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4ce4-134">INPUTS</span></span>

### <span data-ttu-id="b4ce4-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="b4ce4-135">None</span></span>
<span data-ttu-id="b4ce4-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b4ce4-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4ce4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4ce4-137">OUTPUTS</span></span>

## <span data-ttu-id="b4ce4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4ce4-138">NOTES</span></span>

## <span data-ttu-id="b4ce4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4ce4-139">RELATED LINKS</span></span>

[<span data-ttu-id="b4ce4-140">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4ce4-140">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b4ce4-141">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4ce4-141">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b4ce4-142">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4ce4-142">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


