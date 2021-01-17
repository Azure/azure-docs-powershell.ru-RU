---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391191"
---
# <span data-ttu-id="d5151-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d5151-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d5151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5151-102">SYNOPSIS</span></span>
<span data-ttu-id="d5151-103">Удаляет расширение diagnostics (Диагностика) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d5151-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="d5151-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5151-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5151-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5151-105">DESCRIPTION</span></span>
<span data-ttu-id="d5151-106">С **помощью cmdlet Remove-AzVMDiagnosticsExtension** можно удалить расширение для диагностики Azure с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d5151-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="d5151-107">Для реализации изменений необходимо передать результат этого Update-AzVM в этот Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d5151-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="d5151-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5151-108">EXAMPLES</span></span>

### <span data-ttu-id="d5151-109">Пример 1. Удаление расширения диагностики с виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d5151-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="d5151-110">Эта команда удаляет расширение диагностики с виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="d5151-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="d5151-111">Команда передает результат командлету Update-AzVM с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5151-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d5151-112">Эта команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d5151-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="d5151-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5151-113">PARAMETERS</span></span>

### <span data-ttu-id="d5151-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5151-114">-DefaultProfile</span></span>
<span data-ttu-id="d5151-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5151-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5151-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d5151-116">-Name</span></span>
<span data-ttu-id="d5151-117">Указывает имя расширения диагностики, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5151-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d5151-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5151-118">-NoWait</span></span>
<span data-ttu-id="d5151-119">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="d5151-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d5151-120">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="d5151-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d5151-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5151-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5151-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d5151-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d5151-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="d5151-123">-VMName</span></span>
<span data-ttu-id="d5151-124">Указывает имя виртуальной машины, с которой этот cmdlet удаляет расширение для диагностики.</span><span class="sxs-lookup"><span data-stu-id="d5151-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="d5151-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5151-125">CommonParameters</span></span>
<span data-ttu-id="d5151-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5151-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5151-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5151-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5151-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5151-128">INPUTS</span></span>

### <span data-ttu-id="d5151-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5151-129">System.String</span></span>

## <span data-ttu-id="d5151-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5151-130">OUTPUTS</span></span>

### <span data-ttu-id="d5151-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d5151-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d5151-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5151-132">NOTES</span></span>

## <span data-ttu-id="d5151-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5151-133">RELATED LINKS</span></span>

[<span data-ttu-id="d5151-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d5151-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="d5151-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d5151-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="d5151-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d5151-136">Update-AzVM</span></span>](./Update-AzVM.md)


