---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 10c9c634d1435e9460b72bfd1ccdb7e77f7fea53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065065"
---
# <span data-ttu-id="981eb-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="981eb-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="981eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="981eb-102">SYNOPSIS</span></span>
<span data-ttu-id="981eb-103">Добавьте или обновите один или несколько параметров структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="981eb-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="981eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="981eb-104">SYNTAX</span></span>

### <span data-ttu-id="981eb-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="981eb-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="981eb-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="981eb-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="981eb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="981eb-107">DESCRIPTION</span></span>
<span data-ttu-id="981eb-108">С помощью **Set-AzServiceFabricSetting** добавьте или обновите параметры структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="981eb-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="981eb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="981eb-109">EXAMPLES</span></span>

### <span data-ttu-id="981eb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="981eb-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="981eb-111">Эта команда присвойте параметру "MaxFileOperationTimeout" значение "5000" в разделе "NamingService".</span><span class="sxs-lookup"><span data-stu-id="981eb-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="981eb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="981eb-112">PARAMETERS</span></span>

### <span data-ttu-id="981eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981eb-113">-DefaultProfile</span></span>
<span data-ttu-id="981eb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="981eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="981eb-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="981eb-115">-Name</span></span>
<span data-ttu-id="981eb-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="981eb-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="981eb-117">-Параметр</span><span class="sxs-lookup"><span data-stu-id="981eb-117">-Parameter</span></span>
<span data-ttu-id="981eb-118">Имя параметра в параметре "структура"</span><span class="sxs-lookup"><span data-stu-id="981eb-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="981eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="981eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="981eb-120">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="981eb-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="981eb-121">-Раздел</span><span class="sxs-lookup"><span data-stu-id="981eb-121">-Section</span></span>
<span data-ttu-id="981eb-122">Название раздела параметра "структура"</span><span class="sxs-lookup"><span data-stu-id="981eb-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="981eb-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="981eb-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="981eb-124">Массив параметров структуры</span><span class="sxs-lookup"><span data-stu-id="981eb-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="981eb-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="981eb-125">-Value</span></span>
<span data-ttu-id="981eb-126">Значение параметра в параметрах структуры</span><span class="sxs-lookup"><span data-stu-id="981eb-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="981eb-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="981eb-127">-Confirm</span></span>
<span data-ttu-id="981eb-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="981eb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="981eb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="981eb-129">-WhatIf</span></span>
<span data-ttu-id="981eb-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="981eb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="981eb-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="981eb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="981eb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981eb-132">CommonParameters</span></span>
<span data-ttu-id="981eb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="981eb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981eb-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981eb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981eb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="981eb-135">INPUTS</span></span>

### <span data-ttu-id="981eb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="981eb-136">System.String</span></span>

### <span data-ttu-id="981eb-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="981eb-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="981eb-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="981eb-138">OUTPUTS</span></span>

### <span data-ttu-id="981eb-139">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="981eb-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="981eb-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="981eb-140">NOTES</span></span>

## <span data-ttu-id="981eb-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="981eb-141">RELATED LINKS</span></span>
