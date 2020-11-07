---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: cf70191c47f3778268b0087ea542a6812155ebbb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914529"
---
# <span data-ttu-id="0b39f-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b39f-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="0b39f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b39f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b39f-103">Удаляет расширение AEM из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b39f-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b39f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b39f-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b39f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b39f-105">DESCRIPTION</span></span>
<span data-ttu-id="0b39f-106">Командлет **Remove-AzureRmVMAEMExtension** удаляет расширение службы улучшенного мониторинга Azure (AEM) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b39f-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="0b39f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b39f-107">EXAMPLES</span></span>

### <span data-ttu-id="0b39f-108">Пример 1: удаление расширения AEM</span><span class="sxs-lookup"><span data-stu-id="0b39f-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="0b39f-109">Эта команда удаляет расширение AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="0b39f-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="0b39f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b39f-110">PARAMETERS</span></span>

### <span data-ttu-id="0b39f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b39f-111">-DefaultProfile</span></span>
<span data-ttu-id="0b39f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b39f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b39f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b39f-113">-Name</span></span>
<span data-ttu-id="0b39f-114">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение AEM.</span><span class="sxs-lookup"><span data-stu-id="0b39f-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="0b39f-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="0b39f-115">-OSType</span></span>
<span data-ttu-id="0b39f-116">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0b39f-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0b39f-117">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0b39f-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0b39f-118">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="0b39f-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b39f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b39f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b39f-120">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b39f-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="0b39f-121">Этот командлет удаляет расширение AEM из этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b39f-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="0b39f-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="0b39f-122">-VMName</span></span>
<span data-ttu-id="0b39f-123">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0b39f-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0b39f-124">Этот командлет удаляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0b39f-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b39f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b39f-125">CommonParameters</span></span>
<span data-ttu-id="0b39f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b39f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b39f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b39f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b39f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b39f-128">INPUTS</span></span>

### <span data-ttu-id="0b39f-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="0b39f-129">None</span></span>
<span data-ttu-id="0b39f-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0b39f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b39f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b39f-131">OUTPUTS</span></span>

### <span data-ttu-id="0b39f-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b39f-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0b39f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b39f-133">NOTES</span></span>

## <span data-ttu-id="0b39f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b39f-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b39f-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b39f-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="0b39f-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b39f-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="0b39f-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b39f-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


