---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243566"
---
# <span data-ttu-id="4e513-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="4e513-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="4e513-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e513-102">SYNOPSIS</span></span>
<span data-ttu-id="4e513-103">Удаляет центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="4e513-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="4e513-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e513-104">SYNTAX</span></span>

### <span data-ttu-id="4e513-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e513-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e513-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e513-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e513-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e513-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e513-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e513-108">DESCRIPTION</span></span>
<span data-ttu-id="4e513-109">Удаление существующего центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="4e513-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="4e513-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e513-110">EXAMPLES</span></span>

### <span data-ttu-id="4e513-111">Пример 1 удаление и центральное приложение IoT</span><span class="sxs-lookup"><span data-stu-id="4e513-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="4e513-112">Удаляет указанное приложение центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="4e513-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="4e513-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e513-113">PARAMETERS</span></span>

### <span data-ttu-id="4e513-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e513-114">-AsJob</span></span>
<span data-ttu-id="4e513-115">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="4e513-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="4e513-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e513-116">-DefaultProfile</span></span>
<span data-ttu-id="4e513-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e513-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e513-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e513-118">-InputObject</span></span>
<span data-ttu-id="4e513-119">Объект ввода центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="4e513-119">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="4e513-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e513-120">-Name</span></span>
<span data-ttu-id="4e513-121">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="4e513-121">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="4e513-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e513-122">-PassThru</span></span>
<span data-ttu-id="4e513-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="4e513-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4e513-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e513-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e513-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e513-125">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="4e513-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e513-126">-ResourceId</span></span>
<span data-ttu-id="4e513-127">Идентификатор ресурса приложения центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="4e513-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="4e513-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e513-128">-Confirm</span></span>
<span data-ttu-id="4e513-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e513-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e513-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e513-130">-WhatIf</span></span>
<span data-ttu-id="4e513-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e513-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e513-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e513-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e513-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e513-133">CommonParameters</span></span>
<span data-ttu-id="4e513-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e513-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e513-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e513-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e513-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e513-136">INPUTS</span></span>

### <span data-ttu-id="4e513-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4e513-137">System.String</span></span>

### <span data-ttu-id="4e513-138">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="4e513-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="4e513-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e513-139">OUTPUTS</span></span>

### <span data-ttu-id="4e513-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e513-140">System.Boolean</span></span>

## <span data-ttu-id="4e513-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e513-141">NOTES</span></span>

## <span data-ttu-id="4e513-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e513-142">RELATED LINKS</span></span>