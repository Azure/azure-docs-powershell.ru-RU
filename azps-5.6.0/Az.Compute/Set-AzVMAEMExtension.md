---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 4784df2e4ab6d24923bb4c7619e18459101bdf41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004568"
---
# <span data-ttu-id="992e6-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="992e6-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="992e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="992e6-102">SYNOPSIS</span></span>
<span data-ttu-id="992e6-103">Поддержка мониторинга для систем SAP.</span><span class="sxs-lookup"><span data-stu-id="992e6-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="992e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="992e6-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="992e6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="992e6-105">DESCRIPTION</span></span>
<span data-ttu-id="992e6-106">С помощью cmdlet **Set-AzVMAEMExtension** можно обновить конфигурацию виртуальной машины, чтобы включить или обновить поддержку мониторинга для систем SAP, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="992e6-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="992e6-107">Этот cmdlet устанавливает расширение AEM Azure, которое собирает данные о производительности и делает его обнаруживаемым для системы SAP.</span><span class="sxs-lookup"><span data-stu-id="992e6-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="992e6-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="992e6-108">EXAMPLES</span></span>

### <span data-ttu-id="992e6-109">Пример 1. Использование расширения AEM</span><span class="sxs-lookup"><span data-stu-id="992e6-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="992e6-110">Эта команда настраивает виртуальной машине contoso-server для использования расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="992e6-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="992e6-111">Команда определяет учетную запись хранения с именем stdstorage.</span><span class="sxs-lookup"><span data-stu-id="992e6-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="992e6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="992e6-112">PARAMETERS</span></span>

### <span data-ttu-id="992e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992e6-113">-DefaultProfile</span></span>
<span data-ttu-id="992e6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="992e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="992e6-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="992e6-115">-EnableWAD</span></span>
<span data-ttu-id="992e6-116">Если он задан, командлет включает Windows Azure диагностику для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="992e6-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="992e6-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="992e6-117">-InstallNewExtension</span></span>
<span data-ttu-id="992e6-118">Установите новое расширение VM для SAP.</span><span class="sxs-lookup"><span data-stu-id="992e6-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992e6-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="992e6-119">-NoWait</span></span>
<span data-ttu-id="992e6-120">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="992e6-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="992e6-121">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="992e6-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="992e6-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="992e6-122">-OSType</span></span>
<span data-ttu-id="992e6-123">Определяет тип операционной системы на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="992e6-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="992e6-124">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="992e6-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="992e6-125">Допустимыми значениями для этого параметра являются Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="992e6-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="992e6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="992e6-126">-ResourceGroupName</span></span>
<span data-ttu-id="992e6-127">Указывает имя группы ресурсов виртуальной машины, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="992e6-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="992e6-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="992e6-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="992e6-129">Задает доступ удостоверения VM к отдельным ресурсам, например к дискам данных, а не к полной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="992e6-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992e6-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="992e6-130">-SkipStorage</span></span>
<span data-ttu-id="992e6-131">Указывает на то, что этот cmdlet пропускает настройку хранилища.</span><span class="sxs-lookup"><span data-stu-id="992e6-131">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="992e6-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="992e6-132">-VMName</span></span>
<span data-ttu-id="992e6-133">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="992e6-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="992e6-134">Этот cmdlet добавляет расширение AEM для виртуальной машины, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="992e6-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="992e6-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="992e6-135">-WADStorageAccountName</span></span>
<span data-ttu-id="992e6-136">Указывает имя учетной записи хранения, которую этот cmdlet использует для настройки расширения LinuxDiagnostics или IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="992e6-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="992e6-137">Если виртуальная машина не использует стандартную учетную запись хранения, необходимо указать значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="992e6-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="992e6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992e6-138">CommonParameters</span></span>
<span data-ttu-id="992e6-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992e6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992e6-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="992e6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992e6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="992e6-141">INPUTS</span></span>

### <span data-ttu-id="992e6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="992e6-142">System.String</span></span>

## <span data-ttu-id="992e6-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="992e6-143">OUTPUTS</span></span>

### <span data-ttu-id="992e6-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="992e6-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="992e6-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="992e6-145">NOTES</span></span>

## <span data-ttu-id="992e6-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="992e6-146">RELATED LINKS</span></span>

[<span data-ttu-id="992e6-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="992e6-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="992e6-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="992e6-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="992e6-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="992e6-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


