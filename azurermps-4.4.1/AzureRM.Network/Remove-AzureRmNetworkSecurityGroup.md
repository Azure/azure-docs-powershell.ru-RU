---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732563"
---
# <span data-ttu-id="40b0d-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40b0d-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="40b0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="40b0d-103">Удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="40b0d-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40b0d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b0d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="40b0d-106">Командлет **Remove-AzureRmNetworkSecurityGroup** удаляет сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="40b0d-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="40b0d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40b0d-107">EXAMPLES</span></span>

### <span data-ttu-id="40b0d-108">Пример 1: Удаление группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="40b0d-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="40b0d-109">Эта команда удаляет группу безопасности с именем NSG-FrontEnd в группе ресурсов с именем TestRG.</span><span class="sxs-lookup"><span data-stu-id="40b0d-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="40b0d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40b0d-110">PARAMETERS</span></span>

### <span data-ttu-id="40b0d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="40b0d-111">-Force</span></span>
<span data-ttu-id="40b0d-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="40b0d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40b0d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40b0d-113">-Name</span></span>
<span data-ttu-id="40b0d-114">Указывает имя сетевой группы безопасности, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="40b0d-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="40b0d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40b0d-115">-PassThru</span></span>
<span data-ttu-id="40b0d-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="40b0d-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="40b0d-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="40b0d-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="40b0d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b0d-118">-ResourceGroupName</span></span>
<span data-ttu-id="40b0d-119">Указывает имя группы ресурсов, из которой этот командлет удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="40b0d-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="40b0d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40b0d-120">-Confirm</span></span>
<span data-ttu-id="40b0d-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40b0d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b0d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b0d-122">-WhatIf</span></span>
<span data-ttu-id="40b0d-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40b0d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b0d-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40b0d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b0d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b0d-125">-DefaultProfile</span></span>
<span data-ttu-id="40b0d-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40b0d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b0d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b0d-127">CommonParameters</span></span>
<span data-ttu-id="40b0d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40b0d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b0d-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b0d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b0d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40b0d-130">INPUTS</span></span>

## <span data-ttu-id="40b0d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40b0d-131">OUTPUTS</span></span>

## <span data-ttu-id="40b0d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="40b0d-132">NOTES</span></span>

## <span data-ttu-id="40b0d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40b0d-133">RELATED LINKS</span></span>

[<span data-ttu-id="40b0d-134">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40b0d-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="40b0d-135">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40b0d-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="40b0d-136">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40b0d-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


