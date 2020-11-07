---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 36fd9813523a5977c1981e6de54384cf71de7dc5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910452"
---
# <span data-ttu-id="f5d35-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5d35-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="f5d35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5d35-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d35-103">Проверка конфигурации расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="f5d35-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="f5d35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5d35-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5d35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5d35-105">DESCRIPTION</span></span>
<span data-ttu-id="f5d35-106">Командлет **Test-AzVMAEMExtension** проверяет конфигурацию расширения службы улучшенного мониторинга Azure (AEM).</span><span class="sxs-lookup"><span data-stu-id="f5d35-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="f5d35-107">Расширение AEM собирает данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="f5d35-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="f5d35-108">Этот командлет проверяет, доступны ли данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="f5d35-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="f5d35-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5d35-109">EXAMPLES</span></span>

### <span data-ttu-id="f5d35-110">Пример 1: Проверка конфигурации расширения AEM</span><span class="sxs-lookup"><span data-stu-id="f5d35-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="f5d35-111">Эта команда проверяет конфигурацию расширения AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="f5d35-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="f5d35-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5d35-112">PARAMETERS</span></span>

### <span data-ttu-id="f5d35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d35-113">-DefaultProfile</span></span>
<span data-ttu-id="f5d35-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d35-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5d35-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="f5d35-115">-OSType</span></span>
<span data-ttu-id="f5d35-116">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f5d35-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f5d35-117">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f5d35-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f5d35-118">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="f5d35-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="f5d35-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d35-119">-ResourceGroupName</span></span>
<span data-ttu-id="f5d35-120">Указывает имя группы ресурсов виртуальной машины, проверяемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f5d35-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="f5d35-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="f5d35-121">-SkipStorageCheck</span></span>
<span data-ttu-id="f5d35-122">Указывает на то, что этот командлет пропускает проверку конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f5d35-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="f5d35-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="f5d35-123">-VMName</span></span>
<span data-ttu-id="f5d35-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5d35-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f5d35-125">Этот командлет проверяет расширение AEM для виртуальной машины, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f5d35-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5d35-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="f5d35-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="f5d35-127">Задает период ожидания в минутах для проверки конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f5d35-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="f5d35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d35-128">CommonParameters</span></span>
<span data-ttu-id="f5d35-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5d35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d35-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d35-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d35-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5d35-131">INPUTS</span></span>

### <span data-ttu-id="f5d35-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="f5d35-132">None</span></span>
<span data-ttu-id="f5d35-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f5d35-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5d35-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5d35-134">OUTPUTS</span></span>

### <span data-ttu-id="f5d35-135">Microsoft. Azure. Commands. COMPUTE. extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="f5d35-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="f5d35-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5d35-136">NOTES</span></span>

## <span data-ttu-id="f5d35-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5d35-137">RELATED LINKS</span></span>

[<span data-ttu-id="f5d35-138">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5d35-138">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="f5d35-139">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5d35-139">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="f5d35-140">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5d35-140">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


