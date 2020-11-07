---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911415"
---
# <span data-ttu-id="5b716-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5b716-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="5b716-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b716-102">SYNOPSIS</span></span>
<span data-ttu-id="5b716-103">Удаление расширения диагностики из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b716-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="5b716-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b716-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b716-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b716-105">DESCRIPTION</span></span>
<span data-ttu-id="5b716-106">Командлет **Remove-AzVMDiagnosticsExtension** удаляет расширение диагностики Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b716-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="5b716-107">Для реализации изменений необходимо передать результат этого командлета в командлет Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="5b716-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="5b716-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b716-108">EXAMPLES</span></span>

### <span data-ttu-id="5b716-109">Пример 1: удаление расширения диагностики из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5b716-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="5b716-110">Эта команда удаляет расширение диагностики из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="5b716-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="5b716-111">Команда передает результат в командлет Update-AzVM с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5b716-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b716-112">Эта команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5b716-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="5b716-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b716-113">PARAMETERS</span></span>

### <span data-ttu-id="5b716-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b716-114">-DefaultProfile</span></span>
<span data-ttu-id="5b716-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b716-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b716-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b716-116">-Name</span></span>
<span data-ttu-id="5b716-117">Указывает имя расширения диагностики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5b716-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b716-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b716-118">-ResourceGroupName</span></span>
<span data-ttu-id="5b716-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b716-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5b716-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b716-120">-VMName</span></span>
<span data-ttu-id="5b716-121">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="5b716-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="5b716-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b716-122">CommonParameters</span></span>
<span data-ttu-id="5b716-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b716-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b716-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b716-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b716-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b716-125">INPUTS</span></span>

### <span data-ttu-id="5b716-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="5b716-126">None</span></span>
<span data-ttu-id="5b716-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5b716-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b716-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b716-128">OUTPUTS</span></span>

### <span data-ttu-id="5b716-129">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5b716-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5b716-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b716-130">NOTES</span></span>

## <span data-ttu-id="5b716-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b716-131">RELATED LINKS</span></span>

[<span data-ttu-id="5b716-132">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5b716-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="5b716-133">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5b716-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="5b716-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5b716-134">Update-AzVM</span></span>](./Update-AzVM.md)


