---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: 01eb8cba77177ca35f2e1b73ec410baa44e4a58c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913473"
---
# <span data-ttu-id="ba499-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba499-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="ba499-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba499-102">SYNOPSIS</span></span>
<span data-ttu-id="ba499-103">Обеспечивает поддержку наблюдения для систем SAP.</span><span class="sxs-lookup"><span data-stu-id="ba499-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba499-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba499-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba499-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba499-105">DESCRIPTION</span></span>
<span data-ttu-id="ba499-106">Командлет **Set-AzureRmVMAEMExtension** обновляет конфигурацию виртуальной машины, чтобы включить или обновить поддержку наблюдения для систем SAP, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ba499-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="ba499-107">Командлет устанавливает расширение службы улучшенного мониторинга Azure (AEM), которое собирает данные о производительности и делает его обнаруживаемым для системы SAP.</span><span class="sxs-lookup"><span data-stu-id="ba499-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="ba499-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba499-108">EXAMPLES</span></span>

### <span data-ttu-id="ba499-109">Пример 1: использование расширения AEM</span><span class="sxs-lookup"><span data-stu-id="ba499-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="ba499-110">Эта команда настраивает виртуальную машину с именем Contoso-Server на использование расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="ba499-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="ba499-111">Команда задает учетную запись хранения с именем stdstorage.</span><span class="sxs-lookup"><span data-stu-id="ba499-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="ba499-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba499-112">PARAMETERS</span></span>

### <span data-ttu-id="ba499-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba499-113">-DefaultProfile</span></span>
<span data-ttu-id="ba499-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba499-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba499-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="ba499-115">-DisableWAD</span></span>
<span data-ttu-id="ba499-116">Указывает на то, что этот командлет не включает диагностику Azure для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ba499-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="ba499-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="ba499-117">-EnableWAD</span></span>
<span data-ttu-id="ba499-118">Если этот параметр указан, unifiedgroup включит диагностику Windows Azure для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ba499-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="ba499-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="ba499-119">-OSType</span></span>
<span data-ttu-id="ba499-120">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ba499-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ba499-121">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ba499-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ba499-122">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="ba499-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="ba499-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba499-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba499-124">Указывает имя группы ресурсов виртуальной машины, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ba499-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ba499-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="ba499-125">-SkipStorage</span></span>
<span data-ttu-id="ba499-126">Указывает на то, что этот командлет пропускает конфигурацию хранилища.</span><span class="sxs-lookup"><span data-stu-id="ba499-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="ba499-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="ba499-127">-VMName</span></span>
<span data-ttu-id="ba499-128">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ba499-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ba499-129">Этот командлет добавляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ba499-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba499-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba499-130">-WADStorageAccountName</span></span>
<span data-ttu-id="ba499-131">Указывает имя учетной записи хранения, которую этот командлет использует для настройки расширения LinuxDiagnostics или IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="ba499-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="ba499-132">Если виртуальная машина не использует стандартную учетную запись хранения, необходимо указать значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="ba499-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="ba499-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba499-133">CommonParameters</span></span>
<span data-ttu-id="ba499-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba499-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba499-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba499-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba499-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba499-136">INPUTS</span></span>

### <span data-ttu-id="ba499-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="ba499-137">None</span></span>
<span data-ttu-id="ba499-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ba499-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba499-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba499-139">OUTPUTS</span></span>

### <span data-ttu-id="ba499-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ba499-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ba499-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba499-141">NOTES</span></span>

## <span data-ttu-id="ba499-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba499-142">RELATED LINKS</span></span>

[<span data-ttu-id="ba499-143">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba499-143">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ba499-144">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba499-144">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="ba499-145">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba499-145">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


