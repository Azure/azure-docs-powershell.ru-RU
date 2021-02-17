---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233273"
---
# <span data-ttu-id="f3e2e-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f3e2e-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="f3e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e2e-103">Удаляет расширение AEM из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="f3e2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3e2e-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3e2e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3e2e-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e2e-106">Для **удаления расширения AEM** из виртуальной машины удаляется расширение Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="f3e2e-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="f3e2e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3e2e-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e2e-108">Пример 1. Удаление расширения AEM</span><span class="sxs-lookup"><span data-stu-id="f3e2e-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="f3e2e-109">Эта команда удаляет расширение AEM для виртуальной машины с именем contoso-server.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="f3e2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3e2e-110">PARAMETERS</span></span>

### <span data-ttu-id="f3e2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e2e-111">-DefaultProfile</span></span>
<span data-ttu-id="f3e2e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3e2e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f3e2e-113">-Name</span></span>
<span data-ttu-id="f3e2e-114">Указывает имя виртуальной машины, с которой этот cmdlet удаляет расширение AEM.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="f3e2e-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3e2e-115">-NoWait</span></span>
<span data-ttu-id="f3e2e-116">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f3e2e-117">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f3e2e-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="f3e2e-118">-OSType</span></span>
<span data-ttu-id="f3e2e-119">Определяет тип операционной системы на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f3e2e-120">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f3e2e-121">Допустимыми значениями для этого параметра являются Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="f3e2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3e2e-123">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="f3e2e-124">Этот cmdlet удаляет расширение AEM из этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="f3e2e-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f3e2e-125">-VMName</span></span>
<span data-ttu-id="f3e2e-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f3e2e-127">Этот cmdlet удаляет расширение AEM для виртуальной машины, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f3e2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e2e-128">CommonParameters</span></span>
<span data-ttu-id="f3e2e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e2e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3e2e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e2e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3e2e-131">INPUTS</span></span>

### <span data-ttu-id="f3e2e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f3e2e-132">System.String</span></span>

## <span data-ttu-id="f3e2e-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3e2e-133">OUTPUTS</span></span>

### <span data-ttu-id="f3e2e-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f3e2e-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f3e2e-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3e2e-135">NOTES</span></span>

## <span data-ttu-id="f3e2e-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3e2e-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3e2e-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f3e2e-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="f3e2e-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f3e2e-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="f3e2e-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f3e2e-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


