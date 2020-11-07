---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 958ddffb02aaa6c8ac81f413cca6453f7f87c3a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914417"
---
# <span data-ttu-id="3f290-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3f290-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="3f290-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f290-102">SYNOPSIS</span></span>
<span data-ttu-id="3f290-103">Удаление шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3f290-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f290-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f290-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f290-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f290-105">DESCRIPTION</span></span>
<span data-ttu-id="3f290-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="3f290-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="3f290-107">Командлет **Get-AzureRmVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f290-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="3f290-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f290-108">EXAMPLES</span></span>

### <span data-ttu-id="3f290-109">1: Удаление шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3f290-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="3f290-110">Удаляет объект шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="3f290-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="3f290-111">Примечание. необходимо сначала удалить все подключения к шлюзу виртуальной сети с помощью командлета **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="3f290-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="3f290-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f290-112">PARAMETERS</span></span>

### <span data-ttu-id="3f290-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f290-113">-AsJob</span></span>
<span data-ttu-id="3f290-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3f290-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f290-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f290-115">-DefaultProfile</span></span>
<span data-ttu-id="3f290-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f290-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f290-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3f290-117">-Force</span></span>
<span data-ttu-id="3f290-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3f290-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f290-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f290-119">-Name</span></span>
<span data-ttu-id="3f290-120">Указывает имя шлюза виртуальной сети, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3f290-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f290-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f290-121">-PassThru</span></span>
<span data-ttu-id="3f290-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3f290-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f290-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3f290-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f290-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f290-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f290-125">Указывает имя группы ресурсов, которая содержит шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f290-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="3f290-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f290-126">-Confirm</span></span>
<span data-ttu-id="3f290-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f290-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f290-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f290-128">-WhatIf</span></span>
<span data-ttu-id="3f290-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f290-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f290-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f290-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f290-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f290-131">CommonParameters</span></span>
<span data-ttu-id="3f290-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f290-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f290-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f290-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f290-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f290-134">INPUTS</span></span>

## <span data-ttu-id="3f290-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f290-135">OUTPUTS</span></span>

## <span data-ttu-id="3f290-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f290-136">NOTES</span></span>

## <span data-ttu-id="3f290-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f290-137">RELATED LINKS</span></span>

