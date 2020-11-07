---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 22cc09a405d124ef4bf44342077b53dc64f974b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729105"
---
# <span data-ttu-id="f4a09-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f4a09-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="f4a09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4a09-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a09-103">Удалите из кластера один или несколько параметров структуры служб.</span><span class="sxs-lookup"><span data-stu-id="f4a09-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="f4a09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4a09-104">SYNTAX</span></span>

### <span data-ttu-id="f4a09-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="f4a09-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a09-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="f4a09-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a09-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4a09-107">DESCRIPTION</span></span>
<span data-ttu-id="f4a09-108">С помощью **Remove-AzServiceFabricSetting** удалите из кластера параметры структуры обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f4a09-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="f4a09-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4a09-109">EXAMPLES</span></span>

### <span data-ttu-id="f4a09-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4a09-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="f4a09-111">Эта команда удалит параметры "MaxCursors" в разделе "EseStore".</span><span class="sxs-lookup"><span data-stu-id="f4a09-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="f4a09-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4a09-112">PARAMETERS</span></span>

### <span data-ttu-id="f4a09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a09-113">-DefaultProfile</span></span>
<span data-ttu-id="f4a09-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a09-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4a09-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4a09-115">-Name</span></span>
<span data-ttu-id="f4a09-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="f4a09-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f4a09-117">-Параметр</span><span class="sxs-lookup"><span data-stu-id="f4a09-117">-Parameter</span></span>
<span data-ttu-id="f4a09-118">Параметра.</span><span class="sxs-lookup"><span data-stu-id="f4a09-118">Parameter.</span></span>

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

### <span data-ttu-id="f4a09-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a09-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4a09-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4a09-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f4a09-121">-Раздел</span><span class="sxs-lookup"><span data-stu-id="f4a09-121">-Section</span></span>
<span data-ttu-id="f4a09-122">Секци.</span><span class="sxs-lookup"><span data-stu-id="f4a09-122">Section.</span></span>

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

### <span data-ttu-id="f4a09-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="f4a09-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="f4a09-124">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="f4a09-124">Client authentication type.</span></span>

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

### <span data-ttu-id="f4a09-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4a09-125">-Confirm</span></span>
<span data-ttu-id="f4a09-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4a09-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a09-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a09-127">-WhatIf</span></span>
<span data-ttu-id="f4a09-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4a09-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4a09-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4a09-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a09-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a09-130">CommonParameters</span></span>
<span data-ttu-id="f4a09-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4a09-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a09-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a09-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a09-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4a09-133">INPUTS</span></span>

### <span data-ttu-id="f4a09-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a09-134">System.String</span></span>

### <span data-ttu-id="f4a09-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="f4a09-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="f4a09-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4a09-136">OUTPUTS</span></span>

### <span data-ttu-id="f4a09-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="f4a09-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f4a09-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4a09-138">NOTES</span></span>

## <span data-ttu-id="f4a09-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4a09-139">RELATED LINKS</span></span>
