---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 040e7e557934fc90e5609a42c2e553ccf34d2f8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010776"
---
# <span data-ttu-id="8d42f-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8d42f-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="8d42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d42f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d42f-103">Проверяет конфигурацию расширения AEM.</span><span class="sxs-lookup"><span data-stu-id="8d42f-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="8d42f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d42f-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d42f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d42f-105">DESCRIPTION</span></span>
<span data-ttu-id="8d42f-106">Cmdlet **Test-AzVMAEMExtension** проверяет конфигурацию расширения Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="8d42f-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="8d42f-107">Расширение AEM собирает данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="8d42f-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="8d42f-108">Этот cmdlet проверяет, доступны ли данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="8d42f-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="8d42f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d42f-109">EXAMPLES</span></span>

### <span data-ttu-id="8d42f-110">Пример 1. Проверьте конфигурацию расширения AEM</span><span class="sxs-lookup"><span data-stu-id="8d42f-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="8d42f-111">Эта команда проверяет конфигурацию расширения AEM для виртуальной машины с именем contoso-server.</span><span class="sxs-lookup"><span data-stu-id="8d42f-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="8d42f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d42f-112">PARAMETERS</span></span>

### <span data-ttu-id="8d42f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d42f-113">-DefaultProfile</span></span>
<span data-ttu-id="8d42f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d42f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d42f-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="8d42f-115">-OSType</span></span>
<span data-ttu-id="8d42f-116">Определяет тип операционной системы на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8d42f-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="8d42f-117">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8d42f-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="8d42f-118">Допустимыми значениями для этого параметра являются Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="8d42f-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="8d42f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d42f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d42f-120">Указывает имя группы ресурсов виртуальной машины, которую проверяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d42f-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="8d42f-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="8d42f-121">-SkipStorageCheck</span></span>
<span data-ttu-id="8d42f-122">Указывает на то, что этот cmdlet пропускает проверку конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d42f-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="8d42f-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="8d42f-123">-VMName</span></span>
<span data-ttu-id="8d42f-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d42f-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8d42f-125">Этот cmdlet проверяет расширение AEM для виртуальной машины, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8d42f-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d42f-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="8d42f-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="8d42f-127">Время ожидания (в минутах) для проверки конфигурации хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d42f-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="8d42f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d42f-128">CommonParameters</span></span>
<span data-ttu-id="8d42f-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d42f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d42f-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d42f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d42f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d42f-131">INPUTS</span></span>

### <span data-ttu-id="8d42f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8d42f-132">System.String</span></span>

## <span data-ttu-id="8d42f-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d42f-133">OUTPUTS</span></span>

### <span data-ttu-id="8d42f-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="8d42f-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="8d42f-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d42f-135">NOTES</span></span>

## <span data-ttu-id="8d42f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d42f-136">RELATED LINKS</span></span>

[<span data-ttu-id="8d42f-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8d42f-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="8d42f-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8d42f-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="8d42f-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8d42f-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


