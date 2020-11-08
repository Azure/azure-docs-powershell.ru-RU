---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234890"
---
# <span data-ttu-id="e76bb-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="e76bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e76bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e76bb-103">Задает теги для существующего PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="e76bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e76bb-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e76bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e76bb-105">DESCRIPTION</span></span>
<span data-ttu-id="e76bb-106">Командлет **Set-AzPublicIpPrefix** задает теги для префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e76bb-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="e76bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e76bb-107">EXAMPLES</span></span>

### <span data-ttu-id="e76bb-108">Установка префиксов общедоступного IP-адреса для тегов</span><span class="sxs-lookup"><span data-stu-id="e76bb-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="e76bb-109">Первая команда получает существующий общедоступный префикс IP-адреса, вторая команда задает свойство Tags, а третья — обновляет существующий объект.</span><span class="sxs-lookup"><span data-stu-id="e76bb-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="e76bb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e76bb-110">PARAMETERS</span></span>

### <span data-ttu-id="e76bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e76bb-111">-AsJob</span></span>
<span data-ttu-id="e76bb-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e76bb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e76bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76bb-113">-DefaultProfile</span></span>
<span data-ttu-id="e76bb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e76bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e76bb-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-115">-PublicIpPrefix</span></span>
<span data-ttu-id="e76bb-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e76bb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e76bb-117">-Confirm</span></span>
<span data-ttu-id="e76bb-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e76bb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76bb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76bb-119">-WhatIf</span></span>
<span data-ttu-id="e76bb-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e76bb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e76bb-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e76bb-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76bb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76bb-122">CommonParameters</span></span>
<span data-ttu-id="e76bb-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e76bb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76bb-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e76bb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76bb-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e76bb-125">INPUTS</span></span>

### <span data-ttu-id="e76bb-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e76bb-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e76bb-127">OUTPUTS</span></span>

### <span data-ttu-id="e76bb-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e76bb-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e76bb-129">NOTES</span></span>

## <span data-ttu-id="e76bb-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e76bb-130">RELATED LINKS</span></span>

[<span data-ttu-id="e76bb-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="e76bb-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="e76bb-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e76bb-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
