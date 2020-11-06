---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 756d6c9f297faf133f38861879249ba281e65d53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558975"
---
# <span data-ttu-id="e8214-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8214-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="e8214-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8214-102">SYNOPSIS</span></span>
<span data-ttu-id="e8214-103">Удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="e8214-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8214-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8214-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8214-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8214-105">DESCRIPTION</span></span>
<span data-ttu-id="e8214-106">Командлет **Remove-AzureRmNetworkSecurityGroup** удаляет сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="e8214-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="e8214-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8214-107">EXAMPLES</span></span>

### <span data-ttu-id="e8214-108">Пример 1: Удаление группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="e8214-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="e8214-109">Эта команда удаляет группу безопасности с именем NSG-FrontEnd в группе ресурсов с именем TestRG.</span><span class="sxs-lookup"><span data-stu-id="e8214-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="e8214-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8214-110">PARAMETERS</span></span>

### <span data-ttu-id="e8214-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8214-111">-AsJob</span></span>
<span data-ttu-id="e8214-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e8214-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8214-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8214-113">-DefaultProfile</span></span>
<span data-ttu-id="e8214-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8214-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8214-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8214-115">-Force</span></span>
<span data-ttu-id="e8214-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e8214-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e8214-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8214-117">-Name</span></span>
<span data-ttu-id="e8214-118">Указывает имя сетевой группы безопасности, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e8214-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e8214-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8214-119">-PassThru</span></span>
<span data-ttu-id="e8214-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e8214-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8214-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e8214-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8214-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8214-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8214-123">Указывает имя группы ресурсов, из которой этот командлет удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="e8214-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="e8214-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8214-124">-Confirm</span></span>
<span data-ttu-id="e8214-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8214-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8214-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8214-126">-WhatIf</span></span>
<span data-ttu-id="e8214-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8214-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8214-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8214-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8214-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8214-129">CommonParameters</span></span>
<span data-ttu-id="e8214-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8214-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8214-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8214-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8214-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8214-132">INPUTS</span></span>

### <span data-ttu-id="e8214-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8214-133">None</span></span>
<span data-ttu-id="e8214-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e8214-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8214-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8214-135">OUTPUTS</span></span>

## <span data-ttu-id="e8214-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8214-136">NOTES</span></span>

## <span data-ttu-id="e8214-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8214-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8214-138">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8214-138">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="e8214-139">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8214-139">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="e8214-140">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8214-140">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


