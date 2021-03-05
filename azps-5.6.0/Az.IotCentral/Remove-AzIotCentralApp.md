---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 29a53b49e579ab337c2345a15c86c4c27aaffe8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997968"
---
# <span data-ttu-id="a4af4-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a4af4-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="a4af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4af4-102">SYNOPSIS</span></span>
<span data-ttu-id="a4af4-103">Удаляет центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="a4af4-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="a4af4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4af4-104">SYNTAX</span></span>

### <span data-ttu-id="a4af4-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4af4-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4af4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4af4-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4af4-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4af4-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4af4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4af4-108">DESCRIPTION</span></span>
<span data-ttu-id="a4af4-109">Удаляет существующее центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="a4af4-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="a4af4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4af4-110">EXAMPLES</span></span>

### <span data-ttu-id="a4af4-111">Пример 1: "Удаление" и "Центральное приложение IoT"</span><span class="sxs-lookup"><span data-stu-id="a4af4-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="a4af4-112">Удаляет предоставленную центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="a4af4-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="a4af4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4af4-113">PARAMETERS</span></span>

### <span data-ttu-id="a4af4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4af4-114">-AsJob</span></span>
<span data-ttu-id="a4af4-115">Запуск cmdlet в качестве задания в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="a4af4-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="a4af4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4af4-116">-DefaultProfile</span></span>
<span data-ttu-id="a4af4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4af4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4af4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4af4-118">-InputObject</span></span>
<span data-ttu-id="a4af4-119">Объект ввода Iot Central Application.</span><span class="sxs-lookup"><span data-stu-id="a4af4-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4af4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a4af4-120">-Name</span></span>
<span data-ttu-id="a4af4-121">Имя центрального ресурса приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="a4af4-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4af4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4af4-122">-PassThru</span></span>
<span data-ttu-id="a4af4-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a4af4-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a4af4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4af4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4af4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4af4-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4af4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4af4-126">-ResourceId</span></span>
<span data-ttu-id="a4af4-127">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="a4af4-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4af4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4af4-128">-Confirm</span></span>
<span data-ttu-id="a4af4-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4af4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4af4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4af4-130">-WhatIf</span></span>
<span data-ttu-id="a4af4-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4af4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4af4-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a4af4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4af4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4af4-133">CommonParameters</span></span>
<span data-ttu-id="a4af4-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4af4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4af4-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4af4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4af4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4af4-136">INPUTS</span></span>

### <span data-ttu-id="a4af4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a4af4-137">System.String</span></span>

### <span data-ttu-id="a4af4-138">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a4af4-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="a4af4-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4af4-139">OUTPUTS</span></span>

### <span data-ttu-id="a4af4-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4af4-140">System.Boolean</span></span>

## <span data-ttu-id="a4af4-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4af4-141">NOTES</span></span>

## <span data-ttu-id="a4af4-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4af4-142">RELATED LINKS</span></span>
