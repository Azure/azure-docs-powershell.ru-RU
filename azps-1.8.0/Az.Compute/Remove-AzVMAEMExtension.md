---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 9c368da43edcc55f15c9e2322e597bd35a112ece
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731283"
---
# <span data-ttu-id="d43af-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d43af-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="d43af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d43af-102">SYNOPSIS</span></span>
<span data-ttu-id="d43af-103">Удаляет расширение AEM из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d43af-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="d43af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d43af-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d43af-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d43af-105">DESCRIPTION</span></span>
<span data-ttu-id="d43af-106">Командлет **Remove-AzVMAEMExtension** удаляет расширение службы улучшенного мониторинга Azure (AEM) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d43af-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="d43af-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d43af-107">EXAMPLES</span></span>

### <span data-ttu-id="d43af-108">Пример 1: удаление расширения AEM</span><span class="sxs-lookup"><span data-stu-id="d43af-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="d43af-109">Эта команда удаляет расширение AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="d43af-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="d43af-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d43af-110">PARAMETERS</span></span>

### <span data-ttu-id="d43af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43af-111">-DefaultProfile</span></span>
<span data-ttu-id="d43af-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d43af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d43af-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d43af-113">-Name</span></span>
<span data-ttu-id="d43af-114">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение AEM.</span><span class="sxs-lookup"><span data-stu-id="d43af-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="d43af-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="d43af-115">-OSType</span></span>
<span data-ttu-id="d43af-116">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d43af-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d43af-117">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d43af-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d43af-118">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="d43af-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="d43af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43af-119">-ResourceGroupName</span></span>
<span data-ttu-id="d43af-120">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d43af-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="d43af-121">Этот командлет удаляет расширение AEM из этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d43af-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="d43af-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="d43af-122">-VMName</span></span>
<span data-ttu-id="d43af-123">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d43af-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d43af-124">Этот командлет удаляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d43af-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d43af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43af-125">CommonParameters</span></span>
<span data-ttu-id="d43af-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d43af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43af-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43af-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43af-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d43af-128">INPUTS</span></span>

### <span data-ttu-id="d43af-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d43af-129">System.String</span></span>

## <span data-ttu-id="d43af-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d43af-130">OUTPUTS</span></span>

### <span data-ttu-id="d43af-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d43af-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d43af-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d43af-132">NOTES</span></span>

## <span data-ttu-id="d43af-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d43af-133">RELATED LINKS</span></span>

[<span data-ttu-id="d43af-134">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d43af-134">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="d43af-135">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d43af-135">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="d43af-136">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d43af-136">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


