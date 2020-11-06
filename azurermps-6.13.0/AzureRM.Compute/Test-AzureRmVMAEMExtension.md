---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: ab4b746b19f42831b690a61e6300b3205cf7d41b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566536"
---
# <span data-ttu-id="7423a-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7423a-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="7423a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7423a-102">SYNOPSIS</span></span>
<span data-ttu-id="7423a-103">Проверка конфигурации расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="7423a-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7423a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7423a-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7423a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7423a-105">DESCRIPTION</span></span>
<span data-ttu-id="7423a-106">Командлет **Test-AzureRmVMAEMExtension** проверяет конфигурацию расширения службы улучшенного мониторинга Azure (AEM).</span><span class="sxs-lookup"><span data-stu-id="7423a-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="7423a-107">Расширение AEM собирает данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="7423a-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="7423a-108">Этот командлет проверяет, доступны ли данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="7423a-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="7423a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7423a-109">EXAMPLES</span></span>

### <span data-ttu-id="7423a-110">Пример 1: Проверка конфигурации расширения AEM</span><span class="sxs-lookup"><span data-stu-id="7423a-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="7423a-111">Эта команда проверяет конфигурацию расширения AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="7423a-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="7423a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7423a-112">PARAMETERS</span></span>

### <span data-ttu-id="7423a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7423a-113">-DefaultProfile</span></span>
<span data-ttu-id="7423a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7423a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7423a-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="7423a-115">-OSType</span></span>
<span data-ttu-id="7423a-116">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7423a-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="7423a-117">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7423a-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="7423a-118">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="7423a-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7423a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7423a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7423a-120">Указывает имя группы ресурсов виртуальной машины, проверяемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7423a-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="7423a-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="7423a-121">-SkipStorageCheck</span></span>
<span data-ttu-id="7423a-122">Указывает на то, что этот командлет пропускает проверку конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="7423a-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7423a-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="7423a-123">-VMName</span></span>
<span data-ttu-id="7423a-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7423a-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7423a-125">Этот командлет проверяет расширение AEM для виртуальной машины, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7423a-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7423a-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="7423a-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="7423a-127">Задает период ожидания в минутах для проверки конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="7423a-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7423a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7423a-128">CommonParameters</span></span>
<span data-ttu-id="7423a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7423a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7423a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7423a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7423a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7423a-131">INPUTS</span></span>

### <span data-ttu-id="7423a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7423a-132">System.String</span></span>

## <span data-ttu-id="7423a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7423a-133">OUTPUTS</span></span>

### <span data-ttu-id="7423a-134">Microsoft. Azure. Commands. COMPUTE. extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="7423a-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="7423a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="7423a-135">NOTES</span></span>

## <span data-ttu-id="7423a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7423a-136">RELATED LINKS</span></span>

[<span data-ttu-id="7423a-137">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7423a-137">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="7423a-138">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7423a-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="7423a-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7423a-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


