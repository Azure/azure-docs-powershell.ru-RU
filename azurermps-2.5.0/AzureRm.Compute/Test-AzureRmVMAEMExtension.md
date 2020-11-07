---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: ae4a6d72fcb44406773234b6de55cec7ccef8eb9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915350"
---
# <span data-ttu-id="177fc-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="177fc-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="177fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="177fc-102">SYNOPSIS</span></span>
<span data-ttu-id="177fc-103">Проверка конфигурации расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="177fc-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="177fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="177fc-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="177fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="177fc-105">DESCRIPTION</span></span>
<span data-ttu-id="177fc-106">Командлет **Test-AzureRmVMAEMExtension** проверяет конфигурацию расширения службы улучшенного мониторинга Azure (AEM).</span><span class="sxs-lookup"><span data-stu-id="177fc-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="177fc-107">Расширение AEM собирает данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="177fc-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="177fc-108">Этот командлет проверяет, доступны ли данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="177fc-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="177fc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="177fc-109">EXAMPLES</span></span>

### <span data-ttu-id="177fc-110">Пример 1: Проверка конфигурации расширения AEM</span><span class="sxs-lookup"><span data-stu-id="177fc-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="177fc-111">Эта команда проверяет конфигурацию расширения AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="177fc-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="177fc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="177fc-112">PARAMETERS</span></span>

### <span data-ttu-id="177fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177fc-113">-DefaultProfile</span></span>
<span data-ttu-id="177fc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="177fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="177fc-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="177fc-115">-OSType</span></span>
<span data-ttu-id="177fc-116">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="177fc-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="177fc-117">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="177fc-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="177fc-118">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="177fc-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="177fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="177fc-120">Указывает имя группы ресурсов виртуальной машины, проверяемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="177fc-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="177fc-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="177fc-121">-SkipStorageCheck</span></span>
<span data-ttu-id="177fc-122">Указывает на то, что этот командлет пропускает проверку конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="177fc-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="177fc-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="177fc-123">-VMName</span></span>
<span data-ttu-id="177fc-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="177fc-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="177fc-125">Этот командлет проверяет расширение AEM для виртуальной машины, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="177fc-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="177fc-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="177fc-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="177fc-127">Задает период ожидания в минутах для проверки конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="177fc-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="177fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177fc-128">CommonParameters</span></span>
<span data-ttu-id="177fc-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="177fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177fc-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="177fc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177fc-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="177fc-131">INPUTS</span></span>

### <span data-ttu-id="177fc-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="177fc-132">None</span></span>
<span data-ttu-id="177fc-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="177fc-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="177fc-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="177fc-134">OUTPUTS</span></span>

### <span data-ttu-id="177fc-135">Microsoft. Azure. Commands. COMPUTE. extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="177fc-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="177fc-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="177fc-136">NOTES</span></span>

## <span data-ttu-id="177fc-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="177fc-137">RELATED LINKS</span></span>

[<span data-ttu-id="177fc-138">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="177fc-138">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="177fc-139">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="177fc-139">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="177fc-140">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="177fc-140">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


