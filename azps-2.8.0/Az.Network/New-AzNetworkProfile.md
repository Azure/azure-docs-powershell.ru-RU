---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: 87d753ebaf2d8d4891fc96dbc25f7ad0fa1095af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902126"
---
# <span data-ttu-id="32169-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="32169-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="32169-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32169-102">SYNOPSIS</span></span>
<span data-ttu-id="32169-103">Создание нового профиля сети.</span><span class="sxs-lookup"><span data-stu-id="32169-103">Creates a new network profile.</span></span>

## <span data-ttu-id="32169-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32169-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32169-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32169-105">DESCRIPTION</span></span>
<span data-ttu-id="32169-106">Командлет **New-AzNetworkProfile** создает новый ресурс верхнего уровня профиля сети.</span><span class="sxs-lookup"><span data-stu-id="32169-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="32169-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32169-107">EXAMPLES</span></span>

### <span data-ttu-id="32169-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32169-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="32169-109">Это приведет к созданию нового ресурса на высшем уровне сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="32169-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="32169-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32169-110">PARAMETERS</span></span>

### <span data-ttu-id="32169-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32169-111">-AsJob</span></span>
<span data-ttu-id="32169-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="32169-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32169-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="32169-113">-ContainerNicConfig</span></span>
<span data-ttu-id="32169-114">Конфигурации сетевого интерфейса контейнера, добавляемые в этот профиль сети.</span><span class="sxs-lookup"><span data-stu-id="32169-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="32169-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32169-115">-DefaultProfile</span></span>
<span data-ttu-id="32169-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32169-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32169-117">-Force</span><span class="sxs-lookup"><span data-stu-id="32169-117">-Force</span></span>
<span data-ttu-id="32169-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="32169-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32169-119">-Location</span><span class="sxs-lookup"><span data-stu-id="32169-119">-Location</span></span>
<span data-ttu-id="32169-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="32169-120">The location.</span></span>

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

### <span data-ttu-id="32169-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32169-121">-Name</span></span>
<span data-ttu-id="32169-122">Имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="32169-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="32169-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32169-123">-ResourceGroupName</span></span>
<span data-ttu-id="32169-124">Имя группы ресурсов в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="32169-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="32169-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="32169-125">-Tag</span></span>
<span data-ttu-id="32169-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32169-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="32169-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32169-127">-Confirm</span></span>
<span data-ttu-id="32169-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32169-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32169-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32169-129">-WhatIf</span></span>
<span data-ttu-id="32169-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32169-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32169-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32169-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32169-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32169-132">CommonParameters</span></span>
<span data-ttu-id="32169-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32169-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32169-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32169-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32169-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32169-135">INPUTS</span></span>

### <span data-ttu-id="32169-136">System. String</span><span class="sxs-lookup"><span data-stu-id="32169-136">System.String</span></span>

### <span data-ttu-id="32169-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="32169-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="32169-138">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="32169-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="32169-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32169-139">OUTPUTS</span></span>

### <span data-ttu-id="32169-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="32169-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="32169-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="32169-141">NOTES</span></span>

## <span data-ttu-id="32169-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32169-142">RELATED LINKS</span></span>

[<span data-ttu-id="32169-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="32169-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="32169-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="32169-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="32169-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="32169-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
