---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: e463e6a1d25db24553b62c8d2fea1051eb231840
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066532"
---
# <span data-ttu-id="807dd-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="807dd-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="807dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="807dd-102">SYNOPSIS</span></span>
<span data-ttu-id="807dd-103">Создание нового профиля сети.</span><span class="sxs-lookup"><span data-stu-id="807dd-103">Creates a new network profile.</span></span>

## <span data-ttu-id="807dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="807dd-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="807dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="807dd-105">DESCRIPTION</span></span>
<span data-ttu-id="807dd-106">Командлет **New-AzNetworkProfile** создает новый ресурс верхнего уровня профиля сети.</span><span class="sxs-lookup"><span data-stu-id="807dd-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="807dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="807dd-107">EXAMPLES</span></span>

### <span data-ttu-id="807dd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="807dd-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="807dd-109">Это приведет к созданию нового ресурса на высшем уровне сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="807dd-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="807dd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="807dd-110">PARAMETERS</span></span>

### <span data-ttu-id="807dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="807dd-111">-AsJob</span></span>
<span data-ttu-id="807dd-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="807dd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="807dd-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="807dd-113">-ContainerNicConfig</span></span>
<span data-ttu-id="807dd-114">Конфигурации сетевого интерфейса контейнера, добавляемые в этот профиль сети.</span><span class="sxs-lookup"><span data-stu-id="807dd-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="807dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807dd-115">-DefaultProfile</span></span>
<span data-ttu-id="807dd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="807dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="807dd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="807dd-117">-Force</span></span>
<span data-ttu-id="807dd-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="807dd-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="807dd-119">-Location</span><span class="sxs-lookup"><span data-stu-id="807dd-119">-Location</span></span>
<span data-ttu-id="807dd-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="807dd-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="807dd-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="807dd-121">-Name</span></span>
<span data-ttu-id="807dd-122">Имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="807dd-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="807dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="807dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="807dd-124">Имя группы ресурсов в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="807dd-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="807dd-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="807dd-125">-Tag</span></span>
<span data-ttu-id="807dd-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="807dd-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="807dd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="807dd-127">-Confirm</span></span>
<span data-ttu-id="807dd-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="807dd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="807dd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="807dd-129">-WhatIf</span></span>
<span data-ttu-id="807dd-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="807dd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="807dd-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="807dd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="807dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807dd-132">CommonParameters</span></span>
<span data-ttu-id="807dd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="807dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807dd-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="807dd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807dd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="807dd-135">INPUTS</span></span>

### <span data-ttu-id="807dd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="807dd-136">System.String</span></span>

### <span data-ttu-id="807dd-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="807dd-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="807dd-138">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="807dd-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="807dd-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="807dd-139">OUTPUTS</span></span>

### <span data-ttu-id="807dd-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="807dd-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="807dd-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="807dd-141">NOTES</span></span>

## <span data-ttu-id="807dd-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="807dd-142">RELATED LINKS</span></span>

[<span data-ttu-id="807dd-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="807dd-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="807dd-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="807dd-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="807dd-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="807dd-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
