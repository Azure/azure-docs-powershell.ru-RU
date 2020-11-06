---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557495"
---
# <span data-ttu-id="2df51-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2df51-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="2df51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2df51-102">SYNOPSIS</span></span>
<span data-ttu-id="2df51-103">Проверка конфигурации расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="2df51-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2df51-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="2df51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2df51-105">DESCRIPTION</span></span>
<span data-ttu-id="2df51-106">Командлет **Test-AzureRmVMAEMExtension** проверяет конфигурацию расширения службы улучшенного мониторинга Azure (AEM).</span><span class="sxs-lookup"><span data-stu-id="2df51-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="2df51-107">Расширение AEM собирает данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="2df51-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="2df51-108">Этот командлет проверяет, доступны ли данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="2df51-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="2df51-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2df51-109">EXAMPLES</span></span>

### <span data-ttu-id="2df51-110">Пример 1: Проверка конфигурации расширения AEM</span><span class="sxs-lookup"><span data-stu-id="2df51-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="2df51-111">Эта команда проверяет конфигурацию расширения AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="2df51-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="2df51-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2df51-112">PARAMETERS</span></span>

### <span data-ttu-id="2df51-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="2df51-113">-OSType</span></span>
<span data-ttu-id="2df51-114">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2df51-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="2df51-115">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2df51-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="2df51-116">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="2df51-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="2df51-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df51-117">-ResourceGroupName</span></span>
<span data-ttu-id="2df51-118">Указывает имя группы ресурсов виртуальной машины, проверяемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2df51-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="2df51-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="2df51-119">-SkipStorageCheck</span></span>
<span data-ttu-id="2df51-120">Указывает на то, что этот командлет пропускает проверку конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="2df51-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="2df51-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="2df51-121">-VMName</span></span>
<span data-ttu-id="2df51-122">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2df51-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2df51-123">Этот командлет проверяет расширение AEM для виртуальной машины, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2df51-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2df51-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="2df51-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="2df51-125">Задает период ожидания в минутах для проверки конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="2df51-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="2df51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df51-126">CommonParameters</span></span>
<span data-ttu-id="2df51-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2df51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df51-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df51-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df51-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2df51-129">INPUTS</span></span>

### <span data-ttu-id="2df51-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="2df51-130">None</span></span>
<span data-ttu-id="2df51-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2df51-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2df51-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2df51-132">OUTPUTS</span></span>

## <span data-ttu-id="2df51-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2df51-133">NOTES</span></span>

## <span data-ttu-id="2df51-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2df51-134">RELATED LINKS</span></span>

[<span data-ttu-id="2df51-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2df51-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="2df51-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2df51-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="2df51-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2df51-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


