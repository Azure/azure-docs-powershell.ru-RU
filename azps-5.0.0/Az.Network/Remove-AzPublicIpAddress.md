---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248241"
---
# <span data-ttu-id="ea4ee-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4ee-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="ea4ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4ee-103">Удаление общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-103">Removes a public IP address.</span></span>

## <span data-ttu-id="ea4ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea4ee-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea4ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="ea4ee-106">Командлет **Remove-AzPublicIpAddress** удаляет общедоступный IP-адрес Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="ea4ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea4ee-107">EXAMPLES</span></span>

### <span data-ttu-id="ea4ee-108">1: Удаление ресурса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="ea4ee-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="ea4ee-109">Эта команда удаляет ресурс общедоступного IP-адреса с именем $publicIpName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="ea4ee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea4ee-110">PARAMETERS</span></span>

### <span data-ttu-id="ea4ee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea4ee-111">-AsJob</span></span>
<span data-ttu-id="ea4ee-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ea4ee-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea4ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4ee-113">-DefaultProfile</span></span>
<span data-ttu-id="ea4ee-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4ee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ea4ee-115">-Force</span></span>
<span data-ttu-id="ea4ee-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea4ee-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea4ee-117">-Name</span></span>
<span data-ttu-id="ea4ee-118">Указывает имя общедоступного IP-адреса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea4ee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea4ee-119">-PassThru</span></span>
<span data-ttu-id="ea4ee-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea4ee-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea4ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea4ee-123">Указывает имя группы ресурсов, которая содержит общедоступный IP-адрес, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea4ee-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea4ee-124">-Confirm</span></span>
<span data-ttu-id="ea4ee-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea4ee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea4ee-126">-WhatIf</span></span>
<span data-ttu-id="ea4ee-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea4ee-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea4ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4ee-129">CommonParameters</span></span>
<span data-ttu-id="ea4ee-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea4ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4ee-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4ee-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4ee-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea4ee-132">INPUTS</span></span>

### <span data-ttu-id="ea4ee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ea4ee-133">System.String</span></span>

## <span data-ttu-id="ea4ee-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea4ee-134">OUTPUTS</span></span>

### <span data-ttu-id="ea4ee-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea4ee-135">System.Boolean</span></span>

## <span data-ttu-id="ea4ee-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea4ee-136">NOTES</span></span>

## <span data-ttu-id="ea4ee-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea4ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="ea4ee-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4ee-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="ea4ee-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4ee-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ea4ee-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4ee-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


