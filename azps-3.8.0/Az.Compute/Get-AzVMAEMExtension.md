---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 0879458284c7e08b2e8371b9b8d8b894a482a9df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075065"
---
# <span data-ttu-id="ca8f8-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ca8f8-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="ca8f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8f8-103">Получает сведения о расширении AEM.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="ca8f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca8f8-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca8f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca8f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8f8-106">Командлет **Get-AzVMAEMExtension** получает сведения о расширении службы улучшенного мониторинга Azure (AEM).</span><span class="sxs-lookup"><span data-stu-id="ca8f8-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="ca8f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca8f8-107">EXAMPLES</span></span>

### <span data-ttu-id="ca8f8-108">Пример 1: получение расширения AEM</span><span class="sxs-lookup"><span data-stu-id="ca8f8-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ca8f8-109">Эта команда получает сведения о расширении AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ca8f8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca8f8-110">PARAMETERS</span></span>

### <span data-ttu-id="ca8f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8f8-111">-DefaultProfile</span></span>
<span data-ttu-id="ca8f8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca8f8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca8f8-113">-Name</span></span>
<span data-ttu-id="ca8f8-114">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ca8f8-115">Этот командлет получает сведения о расширении AEM на виртуальной машине, указанном этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8f8-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="ca8f8-116">-OSType</span></span>
<span data-ttu-id="ca8f8-117">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ca8f8-118">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ca8f8-119">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8f8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8f8-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca8f8-121">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ca8f8-122">Этот командлет получает сведения о расширении AEM на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="ca8f8-123">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="ca8f8-123">-Status</span></span>
<span data-ttu-id="ca8f8-124">Указывает на то, что этот командлет получает только представление экземпляра для расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8f8-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="ca8f8-125">-VMName</span></span>
<span data-ttu-id="ca8f8-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ca8f8-127">Этот командлет получает сведения о расширении AEM для виртуальной машины, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ca8f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8f8-128">CommonParameters</span></span>
<span data-ttu-id="ca8f8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca8f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8f8-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca8f8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8f8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca8f8-131">INPUTS</span></span>

### <span data-ttu-id="ca8f8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca8f8-132">System.String</span></span>

### <span data-ttu-id="ca8f8-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ca8f8-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ca8f8-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca8f8-134">OUTPUTS</span></span>

### <span data-ttu-id="ca8f8-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ca8f8-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="ca8f8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca8f8-136">NOTES</span></span>

## <span data-ttu-id="ca8f8-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca8f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="ca8f8-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ca8f8-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="ca8f8-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ca8f8-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="ca8f8-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ca8f8-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


