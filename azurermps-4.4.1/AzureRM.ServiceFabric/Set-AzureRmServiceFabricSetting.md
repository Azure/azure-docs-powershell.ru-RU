---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: ef369f67e683a214538f1ecb113f771e2f5cd2f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562124"
---
# <span data-ttu-id="37257-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="37257-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="37257-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37257-102">SYNOPSIS</span></span>
<span data-ttu-id="37257-103">Добавьте или обновите один или несколько параметров структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="37257-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37257-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37257-104">SYNTAX</span></span>

### <span data-ttu-id="37257-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="37257-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37257-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="37257-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37257-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37257-107">DESCRIPTION</span></span>
<span data-ttu-id="37257-108">С помощью **Set-AzureRmServiceFabricSetting** добавьте или обновите параметры структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="37257-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="37257-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37257-109">EXAMPLES</span></span>

### <span data-ttu-id="37257-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37257-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="37257-111">Эта команда присвойте параметру "MaxFileOperationTimeout" значение "5000" в разделе "NamingService".</span><span class="sxs-lookup"><span data-stu-id="37257-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="37257-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37257-112">PARAMETERS</span></span>

### <span data-ttu-id="37257-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37257-113">-Name</span></span>
<span data-ttu-id="37257-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="37257-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="37257-115">-Параметр</span><span class="sxs-lookup"><span data-stu-id="37257-115">-Parameter</span></span>
<span data-ttu-id="37257-116">Параметра.</span><span class="sxs-lookup"><span data-stu-id="37257-116">Parameter.</span></span>

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

### <span data-ttu-id="37257-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37257-117">-ResourceGroupName</span></span>
<span data-ttu-id="37257-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37257-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="37257-119">-Раздел</span><span class="sxs-lookup"><span data-stu-id="37257-119">-Section</span></span>
<span data-ttu-id="37257-120">Секци.</span><span class="sxs-lookup"><span data-stu-id="37257-120">Section.</span></span>

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

### <span data-ttu-id="37257-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="37257-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="37257-122">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="37257-122">Client authentication type.</span></span>

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

### <span data-ttu-id="37257-123">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="37257-123">-Value</span></span>
<span data-ttu-id="37257-124">Значение.</span><span class="sxs-lookup"><span data-stu-id="37257-124">Value.</span></span>

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

### <span data-ttu-id="37257-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37257-125">-Confirm</span></span>
<span data-ttu-id="37257-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37257-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37257-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37257-127">-WhatIf</span></span>
<span data-ttu-id="37257-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37257-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37257-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37257-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37257-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37257-130">-DefaultProfile</span></span>
<span data-ttu-id="37257-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37257-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37257-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37257-132">CommonParameters</span></span>
<span data-ttu-id="37257-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37257-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37257-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37257-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37257-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37257-135">INPUTS</span></span>

### <span data-ttu-id="37257-136">System. String</span><span class="sxs-lookup"><span data-stu-id="37257-136">System.String</span></span>
<span data-ttu-id="37257-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="37257-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="37257-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37257-138">OUTPUTS</span></span>

### <span data-ttu-id="37257-139">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="37257-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="37257-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="37257-140">NOTES</span></span>

## <span data-ttu-id="37257-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37257-141">RELATED LINKS</span></span>

