---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 3250aa7f9108436cadbf0f46ab0e36d3a9c094d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557720"
---
# <span data-ttu-id="13189-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="13189-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="13189-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13189-102">SYNOPSIS</span></span>
<span data-ttu-id="13189-103">Удаление сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="13189-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13189-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13189-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13189-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13189-105">DESCRIPTION</span></span>
<span data-ttu-id="13189-106">Командлет **Remove-AzureRmNetworkInterface** удаляет сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="13189-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="13189-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13189-107">EXAMPLES</span></span>

### <span data-ttu-id="13189-108">Пример 1: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="13189-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="13189-109">Эта команда удаляет сетевую интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="13189-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="13189-110">Так как параметр *Force* не используется, пользователю будет предложено подтвердить это действие.</span><span class="sxs-lookup"><span data-stu-id="13189-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="13189-111">Пример 2: Удаление сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="13189-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="13189-112">Эта команда удаляет все сетевые интерфейсы в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="13189-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="13189-113">Поскольку используется параметр *Force* , пользователь не получает запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="13189-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="13189-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13189-114">PARAMETERS</span></span>

### <span data-ttu-id="13189-115">-Force</span><span class="sxs-lookup"><span data-stu-id="13189-115">-Force</span></span>
<span data-ttu-id="13189-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="13189-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13189-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13189-117">-Name</span></span>
<span data-ttu-id="13189-118">Указывает имя сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="13189-118">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="13189-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13189-119">-PassThru</span></span>
<span data-ttu-id="13189-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="13189-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="13189-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="13189-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13189-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13189-122">-ResourceGroupName</span></span>
<span data-ttu-id="13189-123">Указывает имя группы ресурсов, которая содержит сетевой интерфейс, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="13189-123">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="13189-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13189-124">-Confirm</span></span>
<span data-ttu-id="13189-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13189-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13189-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13189-126">-WhatIf</span></span>
<span data-ttu-id="13189-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13189-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13189-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13189-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13189-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13189-129">-DefaultProfile</span></span>
<span data-ttu-id="13189-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13189-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13189-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13189-131">CommonParameters</span></span>
<span data-ttu-id="13189-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13189-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13189-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13189-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13189-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13189-134">INPUTS</span></span>

## <span data-ttu-id="13189-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13189-135">OUTPUTS</span></span>

## <span data-ttu-id="13189-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="13189-136">NOTES</span></span>

## <span data-ttu-id="13189-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13189-137">RELATED LINKS</span></span>

[<span data-ttu-id="13189-138">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="13189-138">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="13189-139">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="13189-139">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="13189-140">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="13189-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


