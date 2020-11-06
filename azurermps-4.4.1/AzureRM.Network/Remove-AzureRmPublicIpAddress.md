---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 396f603c4a4126b8d438f0048677da7a5dbd7492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565230"
---
# <span data-ttu-id="c0ee5-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0ee5-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="c0ee5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ee5-103">Удаление общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0ee5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0ee5-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0ee5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="c0ee5-106">Командлет **Remove-AzureRmPublicIpAddress** удаляет общедоступный IP-адрес Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="c0ee5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0ee5-107">EXAMPLES</span></span>

### <span data-ttu-id="c0ee5-108">1: Удаление ресурса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="c0ee5-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c0ee5-109">Эта команда удаляет ресурс общедоступного IP-адреса с именем $publicIpName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="c0ee5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0ee5-110">PARAMETERS</span></span>

### <span data-ttu-id="c0ee5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c0ee5-111">-Force</span></span>
<span data-ttu-id="c0ee5-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0ee5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0ee5-113">-Name</span></span>
<span data-ttu-id="c0ee5-114">Указывает имя общедоступного IP-адреса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-114">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c0ee5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0ee5-115">-PassThru</span></span>
<span data-ttu-id="c0ee5-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0ee5-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0ee5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ee5-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0ee5-119">Указывает имя группы ресурсов, которая содержит общедоступный IP-адрес, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-119">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c0ee5-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0ee5-120">-Confirm</span></span>
<span data-ttu-id="c0ee5-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ee5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ee5-122">-WhatIf</span></span>
<span data-ttu-id="c0ee5-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0ee5-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ee5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ee5-125">-DefaultProfile</span></span>
<span data-ttu-id="c0ee5-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0ee5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ee5-127">CommonParameters</span></span>
<span data-ttu-id="c0ee5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0ee5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ee5-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ee5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ee5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0ee5-130">INPUTS</span></span>

## <span data-ttu-id="c0ee5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0ee5-131">OUTPUTS</span></span>

## <span data-ttu-id="c0ee5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0ee5-132">NOTES</span></span>

## <span data-ttu-id="c0ee5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0ee5-133">RELATED LINKS</span></span>

[<span data-ttu-id="c0ee5-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0ee5-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c0ee5-135">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0ee5-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c0ee5-136">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0ee5-136">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


