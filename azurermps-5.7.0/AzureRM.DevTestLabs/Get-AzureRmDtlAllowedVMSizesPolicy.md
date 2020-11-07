---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 25b3f15b6a71b54cbcab1a53f793a32da8b2173a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732534"
---
# <span data-ttu-id="0e17e-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="0e17e-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="0e17e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e17e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e17e-103">Получение политики размеров разрешенных виртуальных машин для лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="0e17e-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e17e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e17e-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e17e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e17e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e17e-106">Командлет **Get-AzureRmDtlAllowedVMSizesPolicy** получает политику допустимых размеров виртуальных машин, которая позволяет указать список допустимых размеров виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="0e17e-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="0e17e-107">Командлет возвращает состояние включения или отключения политики и список всех допустимых размеров виртуальных машин, заданных в указанной политике.</span><span class="sxs-lookup"><span data-stu-id="0e17e-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="0e17e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e17e-108">EXAMPLES</span></span>

## <span data-ttu-id="0e17e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e17e-109">PARAMETERS</span></span>

### <span data-ttu-id="0e17e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e17e-110">-DefaultProfile</span></span>
<span data-ttu-id="0e17e-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0e17e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e17e-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="0e17e-112">-LabName</span></span>
<span data-ttu-id="0e17e-113">Указывает имя лаборатории, для которой этот командлет получает политику размера виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0e17e-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="0e17e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e17e-114">-ResourceGroupName</span></span>
<span data-ttu-id="0e17e-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="0e17e-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e17e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e17e-116">CommonParameters</span></span>
<span data-ttu-id="0e17e-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e17e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e17e-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e17e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e17e-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e17e-119">INPUTS</span></span>

### <span data-ttu-id="0e17e-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="0e17e-120">None</span></span>
<span data-ttu-id="0e17e-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0e17e-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e17e-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e17e-122">OUTPUTS</span></span>

### <span data-ttu-id="0e17e-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0e17e-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="0e17e-124">Этот командлет возвращает политику, которая определяет список размеров виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="0e17e-124">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="0e17e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e17e-125">NOTES</span></span>

## <span data-ttu-id="0e17e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e17e-126">RELATED LINKS</span></span>

[<span data-ttu-id="0e17e-127">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="0e17e-127">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="0e17e-128">Командлеты лаборатории тестирования для разработчиков Azure</span><span class="sxs-lookup"><span data-stu-id="0e17e-128">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


