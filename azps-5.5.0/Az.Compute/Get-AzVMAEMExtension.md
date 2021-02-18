---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 0879458284c7e08b2e8371b9b8d8b894a482a9df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215777"
---
# <span data-ttu-id="15c6f-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="15c6f-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="15c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="15c6f-103">Сведения о расширении AEM.</span><span class="sxs-lookup"><span data-stu-id="15c6f-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="15c6f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="15c6f-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15c6f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15c6f-105">DESCRIPTION</span></span>
<span data-ttu-id="15c6f-106">Для получения сведений о расширении Azure Enhanced Monitoring (AEM) возвращается cmdlet **Get-AzVMAEMExtension.**</span><span class="sxs-lookup"><span data-stu-id="15c6f-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="15c6f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="15c6f-107">EXAMPLES</span></span>

### <span data-ttu-id="15c6f-108">Пример 1. Получить расширение AEM</span><span class="sxs-lookup"><span data-stu-id="15c6f-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="15c6f-109">Эта команда получает сведения о расширении AEM для виртуальной машины с именем contoso-server.</span><span class="sxs-lookup"><span data-stu-id="15c6f-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="15c6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15c6f-110">PARAMETERS</span></span>

### <span data-ttu-id="15c6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c6f-111">-DefaultProfile</span></span>
<span data-ttu-id="15c6f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15c6f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15c6f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="15c6f-113">-Name</span></span>
<span data-ttu-id="15c6f-114">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15c6f-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="15c6f-115">Этот cmdlet получает сведения о расширении AEM на виртуальной машине, которую он указывает.</span><span class="sxs-lookup"><span data-stu-id="15c6f-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="15c6f-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="15c6f-116">-OSType</span></span>
<span data-ttu-id="15c6f-117">Определяет тип операционной системы на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="15c6f-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="15c6f-118">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="15c6f-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="15c6f-119">Допустимыми значениями для этого параметра являются Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="15c6f-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="15c6f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c6f-120">-ResourceGroupName</span></span>
<span data-ttu-id="15c6f-121">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15c6f-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="15c6f-122">Этот cmdlet получает сведения о расширении AEM на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="15c6f-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="15c6f-123">-Status</span><span class="sxs-lookup"><span data-stu-id="15c6f-123">-Status</span></span>
<span data-ttu-id="15c6f-124">Указывает на то, что этот cmdlet получает только представление экземпляра расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="15c6f-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="15c6f-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="15c6f-125">-VMName</span></span>
<span data-ttu-id="15c6f-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15c6f-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="15c6f-127">Этот cmdlet получает сведения о расширении AEM для виртуальной машины, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="15c6f-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="15c6f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c6f-128">CommonParameters</span></span>
<span data-ttu-id="15c6f-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c6f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c6f-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15c6f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c6f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15c6f-131">INPUTS</span></span>

### <span data-ttu-id="15c6f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="15c6f-132">System.String</span></span>

### <span data-ttu-id="15c6f-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15c6f-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15c6f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="15c6f-134">OUTPUTS</span></span>

### <span data-ttu-id="15c6f-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="15c6f-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="15c6f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="15c6f-136">NOTES</span></span>

## <span data-ttu-id="15c6f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15c6f-137">RELATED LINKS</span></span>

[<span data-ttu-id="15c6f-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="15c6f-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="15c6f-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="15c6f-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="15c6f-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="15c6f-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


