---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564236"
---
# <span data-ttu-id="3b059-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3b059-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="3b059-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b059-102">SYNOPSIS</span></span>
<span data-ttu-id="3b059-103">Создание нового профиля сети.</span><span class="sxs-lookup"><span data-stu-id="3b059-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b059-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b059-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b059-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b059-105">DESCRIPTION</span></span>
<span data-ttu-id="3b059-106">Командлет **New-AzureRmNetworkProfile** создает новый ресурс верхнего уровня профиля сети.</span><span class="sxs-lookup"><span data-stu-id="3b059-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="3b059-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b059-107">EXAMPLES</span></span>

### <span data-ttu-id="3b059-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b059-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="3b059-109">Это приведет к созданию нового ресурса на высшем уровне сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="3b059-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="3b059-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b059-110">PARAMETERS</span></span>

### <span data-ttu-id="3b059-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b059-111">-AsJob</span></span>
<span data-ttu-id="3b059-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3b059-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b059-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3b059-113">-ContainerNicConfig</span></span>
<span data-ttu-id="3b059-114">Конфигурации сетевого интерфейса контейнера, добавляемые в этот профиль сети.</span><span class="sxs-lookup"><span data-stu-id="3b059-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="3b059-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b059-115">-DefaultProfile</span></span>
<span data-ttu-id="3b059-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b059-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b059-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3b059-117">-Force</span></span>
<span data-ttu-id="3b059-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="3b059-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3b059-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3b059-119">-Location</span></span>
<span data-ttu-id="3b059-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="3b059-120">The location.</span></span>

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

### <span data-ttu-id="3b059-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b059-121">-Name</span></span>
<span data-ttu-id="3b059-122">Имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="3b059-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="3b059-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b059-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b059-124">Имя группы ресурсов в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="3b059-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="3b059-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="3b059-125">-Tag</span></span>
<span data-ttu-id="3b059-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b059-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3b059-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b059-127">-Confirm</span></span>
<span data-ttu-id="3b059-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b059-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b059-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b059-129">-WhatIf</span></span>
<span data-ttu-id="3b059-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b059-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b059-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b059-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b059-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b059-132">CommonParameters</span></span>
<span data-ttu-id="3b059-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b059-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b059-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b059-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b059-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b059-135">INPUTS</span></span>

### <span data-ttu-id="3b059-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3b059-136">System.String</span></span>

### <span data-ttu-id="3b059-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b059-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3b059-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterface, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="3b059-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3b059-139">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="3b059-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3b059-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b059-140">OUTPUTS</span></span>

### <span data-ttu-id="3b059-141">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3b059-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="3b059-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b059-142">NOTES</span></span>

## <span data-ttu-id="3b059-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b059-143">RELATED LINKS</span></span>
