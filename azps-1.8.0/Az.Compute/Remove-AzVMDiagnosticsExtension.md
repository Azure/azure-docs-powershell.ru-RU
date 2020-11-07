---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bcfc7f3d80c5601d5797d9af2958d2bed6395fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901185"
---
# <span data-ttu-id="28407-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28407-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="28407-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28407-102">SYNOPSIS</span></span>
<span data-ttu-id="28407-103">Удаление расширения диагностики из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28407-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="28407-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28407-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28407-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28407-105">DESCRIPTION</span></span>
<span data-ttu-id="28407-106">Командлет **Remove-AzVMDiagnosticsExtension** удаляет расширение диагностики Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28407-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="28407-107">Для реализации изменений необходимо передать результат этого командлета в командлет Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="28407-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="28407-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28407-108">EXAMPLES</span></span>

### <span data-ttu-id="28407-109">Пример 1: удаление расширения диагностики из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="28407-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="28407-110">Эта команда удаляет расширение диагностики из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="28407-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="28407-111">Команда передает результат в командлет Update-AzVM с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="28407-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="28407-112">Эта команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="28407-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="28407-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28407-113">PARAMETERS</span></span>

### <span data-ttu-id="28407-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28407-114">-DefaultProfile</span></span>
<span data-ttu-id="28407-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28407-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28407-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28407-116">-Name</span></span>
<span data-ttu-id="28407-117">Указывает имя расширения диагностики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="28407-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="28407-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28407-118">-ResourceGroupName</span></span>
<span data-ttu-id="28407-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28407-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="28407-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="28407-120">-VMName</span></span>
<span data-ttu-id="28407-121">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="28407-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="28407-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28407-122">CommonParameters</span></span>
<span data-ttu-id="28407-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28407-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28407-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28407-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28407-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28407-125">INPUTS</span></span>

### <span data-ttu-id="28407-126">System. String</span><span class="sxs-lookup"><span data-stu-id="28407-126">System.String</span></span>

## <span data-ttu-id="28407-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28407-127">OUTPUTS</span></span>

### <span data-ttu-id="28407-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="28407-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="28407-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="28407-129">NOTES</span></span>

## <span data-ttu-id="28407-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28407-130">RELATED LINKS</span></span>

[<span data-ttu-id="28407-131">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28407-131">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="28407-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28407-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="28407-133">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="28407-133">Update-AzVM</span></span>](./Update-AzVM.md)


