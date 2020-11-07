---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: deaa8470a4af38eba1f38581e03165c19b3b18f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721702"
---
# <span data-ttu-id="eedbf-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="eedbf-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="eedbf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eedbf-102">SYNOPSIS</span></span>
<span data-ttu-id="eedbf-103">Обеспечивает поддержку наблюдения для систем SAP.</span><span class="sxs-lookup"><span data-stu-id="eedbf-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="eedbf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eedbf-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eedbf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eedbf-105">DESCRIPTION</span></span>
<span data-ttu-id="eedbf-106">Командлет **Set-AzVMAEMExtension** обновляет конфигурацию виртуальной машины, чтобы включить или обновить поддержку наблюдения для систем SAP, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="eedbf-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="eedbf-107">Командлет устанавливает расширение службы улучшенного мониторинга Azure (AEM), которое собирает данные о производительности и делает его обнаруживаемым для системы SAP.</span><span class="sxs-lookup"><span data-stu-id="eedbf-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="eedbf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eedbf-108">EXAMPLES</span></span>

### <span data-ttu-id="eedbf-109">Пример 1: использование расширения AEM</span><span class="sxs-lookup"><span data-stu-id="eedbf-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="eedbf-110">Эта команда настраивает виртуальную машину с именем Contoso-Server на использование расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="eedbf-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="eedbf-111">Команда задает учетную запись хранения с именем stdstorage.</span><span class="sxs-lookup"><span data-stu-id="eedbf-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="eedbf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eedbf-112">PARAMETERS</span></span>

### <span data-ttu-id="eedbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedbf-113">-DefaultProfile</span></span>
<span data-ttu-id="eedbf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eedbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eedbf-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="eedbf-115">-EnableWAD</span></span>
<span data-ttu-id="eedbf-116">Если этот параметр указан, unifiedgroup включит диагностику Windows Azure для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eedbf-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedbf-117">-Wait</span><span class="sxs-lookup"><span data-stu-id="eedbf-117">-NoWait</span></span>
<span data-ttu-id="eedbf-118">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="eedbf-118">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="eedbf-119">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="eedbf-119">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="eedbf-120">-OSType</span><span class="sxs-lookup"><span data-stu-id="eedbf-120">-OSType</span></span>
<span data-ttu-id="eedbf-121">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="eedbf-121">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="eedbf-122">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eedbf-122">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="eedbf-123">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="eedbf-123">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eedbf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eedbf-124">-ResourceGroupName</span></span>
<span data-ttu-id="eedbf-125">Указывает имя группы ресурсов виртуальной машины, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eedbf-125">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eedbf-126">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="eedbf-126">-SkipStorage</span></span>
<span data-ttu-id="eedbf-127">Указывает на то, что этот командлет пропускает конфигурацию хранилища.</span><span class="sxs-lookup"><span data-stu-id="eedbf-127">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="eedbf-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="eedbf-128">-VMName</span></span>
<span data-ttu-id="eedbf-129">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="eedbf-129">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="eedbf-130">Этот командлет добавляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eedbf-130">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="eedbf-131">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eedbf-131">-WADStorageAccountName</span></span>
<span data-ttu-id="eedbf-132">Указывает имя учетной записи хранения, которую этот командлет использует для настройки расширения LinuxDiagnostics или IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="eedbf-132">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="eedbf-133">Если виртуальная машина не использует стандартную учетную запись хранения, необходимо указать значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="eedbf-133">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="eedbf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedbf-134">CommonParameters</span></span>
<span data-ttu-id="eedbf-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eedbf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedbf-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eedbf-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedbf-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eedbf-137">INPUTS</span></span>

### <span data-ttu-id="eedbf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eedbf-138">System.String</span></span>

## <span data-ttu-id="eedbf-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eedbf-139">OUTPUTS</span></span>

### <span data-ttu-id="eedbf-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eedbf-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eedbf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="eedbf-141">NOTES</span></span>

## <span data-ttu-id="eedbf-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eedbf-142">RELATED LINKS</span></span>

[<span data-ttu-id="eedbf-143">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="eedbf-143">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="eedbf-144">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="eedbf-144">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="eedbf-145">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="eedbf-145">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


