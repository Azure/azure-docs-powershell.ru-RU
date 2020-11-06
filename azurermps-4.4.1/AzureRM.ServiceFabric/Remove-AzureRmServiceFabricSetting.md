---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 6fe4d0c3a32cd96693d64e46f9d8596083dd9c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562127"
---
# <span data-ttu-id="1c884-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1c884-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="1c884-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c884-102">SYNOPSIS</span></span>
<span data-ttu-id="1c884-103">Удалите из кластера один или несколько параметров структуры служб.</span><span class="sxs-lookup"><span data-stu-id="1c884-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c884-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c884-104">SYNTAX</span></span>

### <span data-ttu-id="1c884-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="1c884-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c884-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="1c884-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c884-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c884-107">DESCRIPTION</span></span>
<span data-ttu-id="1c884-108">С помощью **Remove-AzureRmServiceFabricSetting** удалите из кластера параметры структуры обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1c884-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="1c884-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c884-109">EXAMPLES</span></span>

### <span data-ttu-id="1c884-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c884-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="1c884-111">Эта команда удалит параметры "MaxCursors" в разделе "EseStore".</span><span class="sxs-lookup"><span data-stu-id="1c884-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="1c884-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c884-112">PARAMETERS</span></span>

### <span data-ttu-id="1c884-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c884-113">-Name</span></span>
<span data-ttu-id="1c884-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1c884-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c884-115">-Параметр</span><span class="sxs-lookup"><span data-stu-id="1c884-115">-Parameter</span></span>
<span data-ttu-id="1c884-116">Параметра.</span><span class="sxs-lookup"><span data-stu-id="1c884-116">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c884-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c884-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c884-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c884-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c884-119">-Раздел</span><span class="sxs-lookup"><span data-stu-id="1c884-119">-Section</span></span>
<span data-ttu-id="1c884-120">Секци.</span><span class="sxs-lookup"><span data-stu-id="1c884-120">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c884-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="1c884-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="1c884-122">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="1c884-122">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c884-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c884-123">-Confirm</span></span>
<span data-ttu-id="1c884-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c884-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c884-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c884-125">-WhatIf</span></span>
<span data-ttu-id="1c884-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c884-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c884-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c884-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c884-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c884-128">-DefaultProfile</span></span>
<span data-ttu-id="1c884-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c884-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c884-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c884-130">CommonParameters</span></span>
<span data-ttu-id="1c884-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c884-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c884-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c884-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c884-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c884-133">INPUTS</span></span>

### <span data-ttu-id="1c884-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1c884-134">System.String</span></span>
<span data-ttu-id="1c884-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="1c884-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="1c884-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c884-136">OUTPUTS</span></span>

### <span data-ttu-id="1c884-137">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="1c884-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="1c884-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c884-138">NOTES</span></span>

## <span data-ttu-id="1c884-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c884-139">RELATED LINKS</span></span>

