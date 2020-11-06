---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 6d294bd4b6f016ed1731a71528b39adc3bbe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568463"
---
# <span data-ttu-id="1f9bf-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f9bf-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="1f9bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9bf-103">Удаление общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f9bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f9bf-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f9bf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f9bf-105">DESCRIPTION</span></span>
<span data-ttu-id="1f9bf-106">Командлет **Remove-AzureRmPublicIpAddress** удаляет общедоступный IP-адрес Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="1f9bf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f9bf-107">EXAMPLES</span></span>

### <span data-ttu-id="1f9bf-108">1: Удаление ресурса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="1f9bf-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="1f9bf-109">Эта команда удаляет ресурс общедоступного IP-адреса с именем $publicIpName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="1f9bf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f9bf-110">PARAMETERS</span></span>

### <span data-ttu-id="1f9bf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f9bf-111">-AsJob</span></span>
<span data-ttu-id="1f9bf-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1f9bf-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9bf-113">-DefaultProfile</span></span>
<span data-ttu-id="1f9bf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f9bf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f9bf-115">-Force</span></span>
<span data-ttu-id="1f9bf-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9bf-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f9bf-117">-Name</span></span>
<span data-ttu-id="1f9bf-118">Указывает имя общедоступного IP-адреса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9bf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f9bf-119">-PassThru</span></span>
<span data-ttu-id="1f9bf-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f9bf-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9bf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f9bf-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f9bf-123">Указывает имя группы ресурсов, которая содержит общедоступный IP-адрес, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9bf-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f9bf-124">-Confirm</span></span>
<span data-ttu-id="1f9bf-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f9bf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f9bf-126">-WhatIf</span></span>
<span data-ttu-id="1f9bf-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f9bf-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f9bf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9bf-129">CommonParameters</span></span>
<span data-ttu-id="1f9bf-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f9bf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9bf-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f9bf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9bf-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f9bf-132">INPUTS</span></span>

### <span data-ttu-id="1f9bf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f9bf-133">System.String</span></span>

## <span data-ttu-id="1f9bf-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f9bf-134">OUTPUTS</span></span>

### <span data-ttu-id="1f9bf-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f9bf-135">System.Boolean</span></span>

## <span data-ttu-id="1f9bf-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f9bf-136">NOTES</span></span>

## <span data-ttu-id="1f9bf-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f9bf-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f9bf-138">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f9bf-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1f9bf-139">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f9bf-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1f9bf-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f9bf-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


