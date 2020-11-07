---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 87d7ff04b62bcee2e735dacbbdd9ddb3ab04d425
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911354"
---
# <span data-ttu-id="c105f-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c105f-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="c105f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c105f-102">SYNOPSIS</span></span>
<span data-ttu-id="c105f-103">Обеспечивает поддержку наблюдения для систем SAP.</span><span class="sxs-lookup"><span data-stu-id="c105f-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="c105f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c105f-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c105f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c105f-105">DESCRIPTION</span></span>
<span data-ttu-id="c105f-106">Командлет **Set-AzVMAEMExtension** обновляет конфигурацию виртуальной машины, чтобы включить или обновить поддержку наблюдения для систем SAP, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c105f-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="c105f-107">Командлет устанавливает расширение службы улучшенного мониторинга Azure (AEM), которое собирает данные о производительности и делает его обнаруживаемым для системы SAP.</span><span class="sxs-lookup"><span data-stu-id="c105f-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="c105f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c105f-108">EXAMPLES</span></span>

### <span data-ttu-id="c105f-109">Пример 1: использование расширения AEM</span><span class="sxs-lookup"><span data-stu-id="c105f-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="c105f-110">Эта команда настраивает виртуальную машину с именем Contoso-Server на использование расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="c105f-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="c105f-111">Команда задает учетную запись хранения с именем stdstorage.</span><span class="sxs-lookup"><span data-stu-id="c105f-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="c105f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c105f-112">PARAMETERS</span></span>

### <span data-ttu-id="c105f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c105f-113">-DefaultProfile</span></span>
<span data-ttu-id="c105f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c105f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c105f-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="c105f-115">-DisableWAD</span></span>
<span data-ttu-id="c105f-116">Указывает на то, что этот командлет не включает диагностику Azure для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c105f-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="c105f-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="c105f-117">-EnableWAD</span></span>
<span data-ttu-id="c105f-118">Если этот параметр указан, unifiedgroup включит диагностику Windows Azure для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c105f-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c105f-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="c105f-119">-OSType</span></span>
<span data-ttu-id="c105f-120">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c105f-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c105f-121">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c105f-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c105f-122">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="c105f-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c105f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c105f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c105f-124">Указывает имя группы ресурсов виртуальной машины, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c105f-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c105f-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="c105f-125">-SkipStorage</span></span>
<span data-ttu-id="c105f-126">Указывает на то, что этот командлет пропускает конфигурацию хранилища.</span><span class="sxs-lookup"><span data-stu-id="c105f-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="c105f-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="c105f-127">-VMName</span></span>
<span data-ttu-id="c105f-128">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c105f-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c105f-129">Этот командлет добавляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c105f-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c105f-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c105f-130">-WADStorageAccountName</span></span>
<span data-ttu-id="c105f-131">Указывает имя учетной записи хранения, которую этот командлет использует для настройки расширения LinuxDiagnostics или IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="c105f-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="c105f-132">Если виртуальная машина не использует стандартную учетную запись хранения, необходимо указать значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="c105f-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="c105f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c105f-133">CommonParameters</span></span>
<span data-ttu-id="c105f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c105f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c105f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c105f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c105f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c105f-136">INPUTS</span></span>

### <span data-ttu-id="c105f-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="c105f-137">None</span></span>
<span data-ttu-id="c105f-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c105f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c105f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c105f-139">OUTPUTS</span></span>

### <span data-ttu-id="c105f-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c105f-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c105f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c105f-141">NOTES</span></span>

## <span data-ttu-id="c105f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c105f-142">RELATED LINKS</span></span>

[<span data-ttu-id="c105f-143">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c105f-143">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="c105f-144">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c105f-144">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="c105f-145">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c105f-145">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


