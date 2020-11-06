---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 47e1e33f282cbb238c6bbb53bb007d593b9c043f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558804"
---
# <span data-ttu-id="0e162-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0e162-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="0e162-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e162-102">SYNOPSIS</span></span>
<span data-ttu-id="0e162-103">Удалите из кластера один или несколько параметров структуры служб.</span><span class="sxs-lookup"><span data-stu-id="0e162-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e162-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e162-104">SYNTAX</span></span>

### <span data-ttu-id="0e162-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="0e162-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e162-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="0e162-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e162-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e162-107">DESCRIPTION</span></span>
<span data-ttu-id="0e162-108">С помощью **Remove-AzureRmServiceFabricSetting** удалите из кластера параметры структуры обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0e162-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="0e162-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e162-109">EXAMPLES</span></span>

### <span data-ttu-id="0e162-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e162-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="0e162-111">Эта команда удалит параметры "MaxCursors" в разделе "EseStore".</span><span class="sxs-lookup"><span data-stu-id="0e162-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="0e162-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e162-112">PARAMETERS</span></span>

### <span data-ttu-id="0e162-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e162-113">-DefaultProfile</span></span>
<span data-ttu-id="0e162-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e162-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e162-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e162-115">-Name</span></span>
<span data-ttu-id="0e162-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="0e162-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e162-117">-Параметр</span><span class="sxs-lookup"><span data-stu-id="0e162-117">-Parameter</span></span>
<span data-ttu-id="0e162-118">Параметра.</span><span class="sxs-lookup"><span data-stu-id="0e162-118">Parameter.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e162-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e162-119">-ResourceGroupName</span></span>
<span data-ttu-id="0e162-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e162-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e162-121">-Раздел</span><span class="sxs-lookup"><span data-stu-id="0e162-121">-Section</span></span>
<span data-ttu-id="0e162-122">Секци.</span><span class="sxs-lookup"><span data-stu-id="0e162-122">Section.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e162-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="0e162-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="0e162-124">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="0e162-124">Client authentication type.</span></span>

```yaml
Type: PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e162-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e162-125">-Confirm</span></span>
<span data-ttu-id="0e162-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e162-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e162-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e162-127">-WhatIf</span></span>
<span data-ttu-id="0e162-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e162-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e162-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e162-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e162-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e162-130">CommonParameters</span></span>
<span data-ttu-id="0e162-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e162-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e162-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e162-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e162-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e162-133">INPUTS</span></span>

### <span data-ttu-id="0e162-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0e162-134">System.String</span></span>
<span data-ttu-id="0e162-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="0e162-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="0e162-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e162-136">OUTPUTS</span></span>

### <span data-ttu-id="0e162-137">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="0e162-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="0e162-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e162-138">NOTES</span></span>

## <span data-ttu-id="0e162-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e162-139">RELATED LINKS</span></span>

