---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: af8a85c698a59a31516c6dee05bb57415a45ff62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913777"
---
# <span data-ttu-id="bc4bc-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc4bc-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="bc4bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4bc-103">Удаление общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc4bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc4bc-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc4bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc4bc-105">DESCRIPTION</span></span>
<span data-ttu-id="bc4bc-106">Командлет **Remove-AzureRmPublicIpAddress** удаляет общедоступный IP-адрес Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="bc4bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc4bc-107">EXAMPLES</span></span>

### <span data-ttu-id="bc4bc-108">1: Удаление ресурса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="bc4bc-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="bc4bc-109">Эта команда удаляет ресурс общедоступного IP-адреса с именем $publicIpName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="bc4bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc4bc-110">PARAMETERS</span></span>

### <span data-ttu-id="bc4bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc4bc-111">-AsJob</span></span>
<span data-ttu-id="bc4bc-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bc4bc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc4bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4bc-113">-DefaultProfile</span></span>
<span data-ttu-id="bc4bc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc4bc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bc4bc-115">-Force</span></span>
<span data-ttu-id="bc4bc-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc4bc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc4bc-117">-Name</span></span>
<span data-ttu-id="bc4bc-118">Указывает имя общедоступного IP-адреса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc4bc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc4bc-119">-PassThru</span></span>
<span data-ttu-id="bc4bc-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bc4bc-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bc4bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc4bc-123">Указывает имя группы ресурсов, которая содержит общедоступный IP-адрес, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc4bc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc4bc-124">-Confirm</span></span>
<span data-ttu-id="bc4bc-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc4bc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4bc-126">-WhatIf</span></span>
<span data-ttu-id="bc4bc-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc4bc-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc4bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4bc-129">CommonParameters</span></span>
<span data-ttu-id="bc4bc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc4bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4bc-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc4bc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4bc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc4bc-132">INPUTS</span></span>

## <span data-ttu-id="bc4bc-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc4bc-133">OUTPUTS</span></span>

## <span data-ttu-id="bc4bc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc4bc-134">NOTES</span></span>

## <span data-ttu-id="bc4bc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc4bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="bc4bc-136">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc4bc-136">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="bc4bc-137">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc4bc-137">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="bc4bc-138">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc4bc-138">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


