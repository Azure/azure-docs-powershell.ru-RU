---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248807"
---
# <span data-ttu-id="59d6f-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="59d6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="59d6f-103">Задает теги для существующего PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="59d6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59d6f-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d6f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="59d6f-106">Командлет **Set-AzPublicIpPrefix** задает теги для префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="59d6f-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="59d6f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="59d6f-108">Установка префиксов общедоступного IP-адреса для тегов</span><span class="sxs-lookup"><span data-stu-id="59d6f-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="59d6f-109">Первая команда получает существующий общедоступный префикс IP-адреса, вторая команда задает свойство Tags, а третья — обновляет существующий объект.</span><span class="sxs-lookup"><span data-stu-id="59d6f-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="59d6f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59d6f-110">PARAMETERS</span></span>

### <span data-ttu-id="59d6f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59d6f-111">-AsJob</span></span>
<span data-ttu-id="59d6f-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="59d6f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59d6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d6f-113">-DefaultProfile</span></span>
<span data-ttu-id="59d6f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59d6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d6f-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-115">-PublicIpPrefix</span></span>
<span data-ttu-id="59d6f-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="59d6f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59d6f-117">-Confirm</span></span>
<span data-ttu-id="59d6f-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59d6f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d6f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d6f-119">-WhatIf</span></span>
<span data-ttu-id="59d6f-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59d6f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d6f-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59d6f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d6f-122">CommonParameters</span></span>
<span data-ttu-id="59d6f-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59d6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d6f-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d6f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d6f-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59d6f-125">INPUTS</span></span>

### <span data-ttu-id="59d6f-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="59d6f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d6f-127">OUTPUTS</span></span>

### <span data-ttu-id="59d6f-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="59d6f-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="59d6f-129">NOTES</span></span>

## <span data-ttu-id="59d6f-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59d6f-130">RELATED LINKS</span></span>

[<span data-ttu-id="59d6f-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="59d6f-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="59d6f-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="59d6f-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)