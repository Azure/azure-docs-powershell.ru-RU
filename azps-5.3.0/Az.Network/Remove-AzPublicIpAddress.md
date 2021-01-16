---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519960"
---
# <span data-ttu-id="6a2e0-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a2e0-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="6a2e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2e0-103">Удаляет общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-103">Removes a public IP address.</span></span>

## <span data-ttu-id="6a2e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a2e0-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a2e0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a2e0-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2e0-106">С **помощью cmdlet Remove-AzPublicIpAddress** удаляется общедоступный IP-адрес Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="6a2e0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a2e0-107">EXAMPLES</span></span>

### <span data-ttu-id="6a2e0-108">1. Удаление ресурса с общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="6a2e0-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="6a2e0-109">Эта команда удаляет общедоступный IP-адрес ресурса $publicIpName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="6a2e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a2e0-110">PARAMETERS</span></span>

### <span data-ttu-id="6a2e0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a2e0-111">-AsJob</span></span>
<span data-ttu-id="6a2e0-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6a2e0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a2e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2e0-113">-DefaultProfile</span></span>
<span data-ttu-id="6a2e0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a2e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6a2e0-115">-Force</span></span>
<span data-ttu-id="6a2e0-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a2e0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6a2e0-117">-Name</span></span>
<span data-ttu-id="6a2e0-118">Указывает имя общего IP-адреса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a2e0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a2e0-119">-PassThru</span></span>
<span data-ttu-id="6a2e0-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a2e0-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a2e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a2e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a2e0-123">Имя группы ресурсов, которая содержит общедоступный IP-адрес, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a2e0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a2e0-124">-Confirm</span></span>
<span data-ttu-id="6a2e0-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a2e0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a2e0-126">-WhatIf</span></span>
<span data-ttu-id="6a2e0-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a2e0-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a2e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2e0-129">CommonParameters</span></span>
<span data-ttu-id="6a2e0-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2e0-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2e0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2e0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a2e0-132">INPUTS</span></span>

### <span data-ttu-id="6a2e0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6a2e0-133">System.String</span></span>

## <span data-ttu-id="6a2e0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a2e0-134">OUTPUTS</span></span>

### <span data-ttu-id="6a2e0-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a2e0-135">System.Boolean</span></span>

## <span data-ttu-id="6a2e0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a2e0-136">NOTES</span></span>

## <span data-ttu-id="6a2e0-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a2e0-137">RELATED LINKS</span></span>

[<span data-ttu-id="6a2e0-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a2e0-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="6a2e0-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a2e0-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="6a2e0-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a2e0-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)

