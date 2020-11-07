---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: d2027ac9778324cf1f0e39d4b5b6f5b7fe37b178
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721766"
---
# <span data-ttu-id="5c8ac-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5c8ac-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="5c8ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8ac-103">Удаление расширения диагностики из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="5c8ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c8ac-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c8ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="5c8ac-106">Командлет **Remove-AzVMDiagnosticsExtension** удаляет расширение диагностики Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="5c8ac-107">Для реализации изменений необходимо передать результат этого командлета в командлет Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="5c8ac-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c8ac-108">EXAMPLES</span></span>

### <span data-ttu-id="5c8ac-109">Пример 1: удаление расширения диагностики из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5c8ac-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="5c8ac-110">Эта команда удаляет расширение диагностики из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="5c8ac-111">Команда передает результат в командлет Update-AzVM с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5c8ac-112">Эта команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="5c8ac-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c8ac-113">PARAMETERS</span></span>

### <span data-ttu-id="5c8ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8ac-114">-DefaultProfile</span></span>
<span data-ttu-id="5c8ac-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c8ac-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c8ac-116">-Name</span></span>
<span data-ttu-id="5c8ac-117">Указывает имя расширения диагностики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5c8ac-118">-Wait</span><span class="sxs-lookup"><span data-stu-id="5c8ac-118">-NoWait</span></span>
<span data-ttu-id="5c8ac-119">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5c8ac-120">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5c8ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c8ac-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5c8ac-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="5c8ac-123">-VMName</span></span>
<span data-ttu-id="5c8ac-124">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="5c8ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8ac-125">CommonParameters</span></span>
<span data-ttu-id="5c8ac-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c8ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8ac-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c8ac-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8ac-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c8ac-128">INPUTS</span></span>

### <span data-ttu-id="5c8ac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5c8ac-129">System.String</span></span>

## <span data-ttu-id="5c8ac-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c8ac-130">OUTPUTS</span></span>

### <span data-ttu-id="5c8ac-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5c8ac-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5c8ac-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c8ac-132">NOTES</span></span>

## <span data-ttu-id="5c8ac-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c8ac-133">RELATED LINKS</span></span>

[<span data-ttu-id="5c8ac-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5c8ac-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="5c8ac-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5c8ac-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="5c8ac-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c8ac-136">Update-AzVM</span></span>](./Update-AzVM.md)


