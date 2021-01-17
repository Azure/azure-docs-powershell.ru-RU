---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413063"
---
# <span data-ttu-id="87a10-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="87a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a10-102">SYNOPSIS</span></span>
<span data-ttu-id="87a10-103">Задает теги для существующего publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="87a10-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="87a10-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87a10-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87a10-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87a10-105">DESCRIPTION</span></span>
<span data-ttu-id="87a10-106">Командлет **Set-AzPublicIpPrefix** задает теги для префикса общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="87a10-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="87a10-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87a10-107">EXAMPLES</span></span>

### <span data-ttu-id="87a10-108">Настройка тегов для префикса общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="87a10-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="87a10-109">Первая команда получает существующий префикс общего IP-адреса, вторая задает свойство "Теги", а третья команда обновляет существующий объект.</span><span class="sxs-lookup"><span data-stu-id="87a10-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="87a10-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87a10-110">PARAMETERS</span></span>

### <span data-ttu-id="87a10-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87a10-111">-AsJob</span></span>
<span data-ttu-id="87a10-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="87a10-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87a10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a10-113">-DefaultProfile</span></span>
<span data-ttu-id="87a10-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87a10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a10-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-115">-PublicIpPrefix</span></span>
<span data-ttu-id="87a10-116">The PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="87a10-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87a10-117">-Confirm</span></span>
<span data-ttu-id="87a10-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="87a10-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a10-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a10-119">-WhatIf</span></span>
<span data-ttu-id="87a10-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87a10-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a10-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="87a10-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a10-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a10-122">CommonParameters</span></span>
<span data-ttu-id="87a10-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a10-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a10-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a10-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a10-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87a10-125">INPUTS</span></span>

### <span data-ttu-id="87a10-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="87a10-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87a10-127">OUTPUTS</span></span>

### <span data-ttu-id="87a10-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="87a10-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87a10-129">NOTES</span></span>

## <span data-ttu-id="87a10-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87a10-130">RELATED LINKS</span></span>

[<span data-ttu-id="87a10-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="87a10-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="87a10-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="87a10-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
