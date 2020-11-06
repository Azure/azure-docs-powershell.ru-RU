---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 829dc03dad037b6b1576613ab18d9929a777241e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558988"
---
# <span data-ttu-id="6f21d-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6f21d-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="6f21d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f21d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f21d-103">Удаление сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6f21d-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f21d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f21d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f21d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f21d-105">DESCRIPTION</span></span>
<span data-ttu-id="6f21d-106">Командлет **Remove-AzureRmNetworkInterface** удаляет сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="6f21d-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="6f21d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f21d-107">EXAMPLES</span></span>

### <span data-ttu-id="6f21d-108">Пример 1: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="6f21d-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="6f21d-109">Эта команда удаляет сетевую интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="6f21d-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="6f21d-110">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="6f21d-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="6f21d-111">Пример 2: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="6f21d-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="6f21d-112">Эта команда удаляет все сетевые интерфейсы в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="6f21d-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="6f21d-113">Поскольку используется параметр *Force* , пользователь не получает запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6f21d-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="6f21d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f21d-114">PARAMETERS</span></span>

### <span data-ttu-id="6f21d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f21d-115">-AsJob</span></span>
<span data-ttu-id="6f21d-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6f21d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f21d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f21d-117">-DefaultProfile</span></span>
<span data-ttu-id="6f21d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f21d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f21d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6f21d-119">-Force</span></span>
<span data-ttu-id="6f21d-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f21d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f21d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f21d-121">-Name</span></span>
<span data-ttu-id="6f21d-122">Указывает имя сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6f21d-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6f21d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f21d-123">-PassThru</span></span>
<span data-ttu-id="6f21d-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6f21d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f21d-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6f21d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6f21d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f21d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f21d-127">Указывает имя группы ресурсов, которая содержит сетевой интерфейс, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6f21d-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6f21d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f21d-128">-Confirm</span></span>
<span data-ttu-id="6f21d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f21d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f21d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f21d-130">-WhatIf</span></span>
<span data-ttu-id="6f21d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f21d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f21d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f21d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f21d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f21d-133">CommonParameters</span></span>
<span data-ttu-id="6f21d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f21d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f21d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f21d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f21d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f21d-136">INPUTS</span></span>

### <span data-ttu-id="6f21d-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="6f21d-137">None</span></span>
<span data-ttu-id="6f21d-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6f21d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f21d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f21d-139">OUTPUTS</span></span>

## <span data-ttu-id="6f21d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f21d-140">NOTES</span></span>

## <span data-ttu-id="6f21d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f21d-141">RELATED LINKS</span></span>

[<span data-ttu-id="6f21d-142">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6f21d-142">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="6f21d-143">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6f21d-143">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="6f21d-144">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6f21d-144">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


