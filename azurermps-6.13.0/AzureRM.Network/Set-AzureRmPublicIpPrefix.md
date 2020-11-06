---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556583"
---
# <span data-ttu-id="329bf-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="329bf-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="329bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="329bf-102">SYNOPSIS</span></span>
<span data-ttu-id="329bf-103">Задает теги для существующего PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="329bf-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="329bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="329bf-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329bf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="329bf-105">DESCRIPTION</span></span>
<span data-ttu-id="329bf-106">Командлет **Set-AzureRmPublicIpPrefix** задает теги для префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="329bf-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="329bf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="329bf-107">EXAMPLES</span></span>

### <span data-ttu-id="329bf-108">Установка префиксов общедоступного IP-адреса для тегов</span><span class="sxs-lookup"><span data-stu-id="329bf-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="329bf-109">Первая команда получает существующий общедоступный префикс IP-адреса, вторая команда задает свойство Tags, а третья — обновляет существующий объект.</span><span class="sxs-lookup"><span data-stu-id="329bf-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="329bf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="329bf-110">PARAMETERS</span></span>

### <span data-ttu-id="329bf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="329bf-111">-AsJob</span></span>
<span data-ttu-id="329bf-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="329bf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="329bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329bf-113">-DefaultProfile</span></span>
<span data-ttu-id="329bf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="329bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="329bf-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="329bf-115">-PublicIpPrefix</span></span>
<span data-ttu-id="329bf-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="329bf-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="329bf-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="329bf-117">-Confirm</span></span>
<span data-ttu-id="329bf-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="329bf-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329bf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329bf-119">-WhatIf</span></span>
<span data-ttu-id="329bf-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="329bf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329bf-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="329bf-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329bf-122">CommonParameters</span></span>
<span data-ttu-id="329bf-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="329bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="329bf-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="329bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329bf-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="329bf-125">INPUTS</span></span>

### <span data-ttu-id="329bf-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="329bf-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="329bf-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="329bf-127">OUTPUTS</span></span>

### <span data-ttu-id="329bf-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="329bf-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="329bf-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="329bf-129">NOTES</span></span>

## <span data-ttu-id="329bf-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="329bf-130">RELATED LINKS</span></span>
