---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/remove-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
ms.openlocfilehash: c8a2f32b82a6111c1117a4134f0f7fe8b96a966f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569843"
---
# <span data-ttu-id="73342-101">Remove-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="73342-101">Remove-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="73342-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73342-102">SYNOPSIS</span></span>
<span data-ttu-id="73342-103">Удаляет центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="73342-103">Deletes an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73342-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73342-104">SYNTAX</span></span>

### <span data-ttu-id="73342-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73342-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73342-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73342-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73342-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="73342-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73342-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73342-108">DESCRIPTION</span></span>
<span data-ttu-id="73342-109">Удаление существующего центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="73342-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="73342-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73342-110">EXAMPLES</span></span>

### <span data-ttu-id="73342-111">Пример 1 удаление и центральное приложение IoT</span><span class="sxs-lookup"><span data-stu-id="73342-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="73342-112">Удаляет указанное приложение центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="73342-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="73342-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73342-113">PARAMETERS</span></span>

### <span data-ttu-id="73342-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73342-114">-AsJob</span></span>
<span data-ttu-id="73342-115">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="73342-115">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73342-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73342-116">-DefaultProfile</span></span>
<span data-ttu-id="73342-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73342-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73342-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73342-118">-InputObject</span></span>
<span data-ttu-id="73342-119">Объект ввода центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="73342-119">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73342-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73342-120">-Name</span></span>
<span data-ttu-id="73342-121">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="73342-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73342-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73342-122">-PassThru</span></span>
<span data-ttu-id="73342-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="73342-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73342-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73342-124">-ResourceGroupName</span></span>
<span data-ttu-id="73342-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73342-125">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73342-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73342-126">-ResourceId</span></span>
<span data-ttu-id="73342-127">Идентификатор ресурса приложения центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="73342-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73342-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73342-128">-Confirm</span></span>
<span data-ttu-id="73342-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73342-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73342-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73342-130">-WhatIf</span></span>
<span data-ttu-id="73342-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73342-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73342-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73342-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73342-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73342-133">CommonParameters</span></span>
<span data-ttu-id="73342-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73342-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73342-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73342-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73342-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73342-136">INPUTS</span></span>

### <span data-ttu-id="73342-137">System. String</span><span class="sxs-lookup"><span data-stu-id="73342-137">System.String</span></span>
### <span data-ttu-id="73342-138">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="73342-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="73342-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73342-139">OUTPUTS</span></span>

### <span data-ttu-id="73342-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73342-140">System.Boolean</span></span>
## <span data-ttu-id="73342-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="73342-141">NOTES</span></span>

## <span data-ttu-id="73342-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73342-142">RELATED LINKS</span></span>
