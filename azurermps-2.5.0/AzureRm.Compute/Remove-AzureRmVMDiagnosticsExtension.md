---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 57e3aef7ff5b6acece0ccba1505d33f2add05ae2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914217"
---
# <span data-ttu-id="87da5-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="87da5-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="87da5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87da5-102">SYNOPSIS</span></span>
<span data-ttu-id="87da5-103">Удаление расширения диагностики из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="87da5-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87da5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87da5-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87da5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87da5-105">DESCRIPTION</span></span>
<span data-ttu-id="87da5-106">Командлет **Remove-AzureRmVMDiagnosticsExtension** удаляет расширение диагностики Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="87da5-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="87da5-107">Для реализации изменений необходимо передать результат этого командлета в командлет Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="87da5-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="87da5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87da5-108">EXAMPLES</span></span>

### <span data-ttu-id="87da5-109">Пример 1: удаление расширения диагностики из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="87da5-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="87da5-110">Эта команда удаляет расширение диагностики из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="87da5-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="87da5-111">Команда передает результат в командлет Update-AzureRmVM с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="87da5-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87da5-112">Эта команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="87da5-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="87da5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87da5-113">PARAMETERS</span></span>

### <span data-ttu-id="87da5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87da5-114">-DefaultProfile</span></span>
<span data-ttu-id="87da5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87da5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87da5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87da5-116">-Name</span></span>
<span data-ttu-id="87da5-117">Указывает имя расширения диагностики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="87da5-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="87da5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87da5-118">-ResourceGroupName</span></span>
<span data-ttu-id="87da5-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="87da5-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="87da5-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="87da5-120">-VMName</span></span>
<span data-ttu-id="87da5-121">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="87da5-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="87da5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87da5-122">CommonParameters</span></span>
<span data-ttu-id="87da5-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87da5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87da5-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87da5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87da5-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87da5-125">INPUTS</span></span>

### <span data-ttu-id="87da5-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="87da5-126">None</span></span>
<span data-ttu-id="87da5-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="87da5-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87da5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87da5-128">OUTPUTS</span></span>

### <span data-ttu-id="87da5-129">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="87da5-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="87da5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="87da5-130">NOTES</span></span>

## <span data-ttu-id="87da5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87da5-131">RELATED LINKS</span></span>

[<span data-ttu-id="87da5-132">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="87da5-132">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="87da5-133">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="87da5-133">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="87da5-134">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="87da5-134">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


