---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 420226346f89b480c283a190ee54f87cde2de005
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721088"
---
# <span data-ttu-id="48f02-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="48f02-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="48f02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48f02-102">SYNOPSIS</span></span>
<span data-ttu-id="48f02-103">Получение политики размеров разрешенных виртуальных машин для лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="48f02-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="48f02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48f02-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48f02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48f02-105">DESCRIPTION</span></span>
<span data-ttu-id="48f02-106">Командлет **Get-AzDtlAllowedVMSizesPolicy** получает политику допустимых размеров виртуальных машин, которая позволяет указать список допустимых размеров виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="48f02-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="48f02-107">Командлет возвращает состояние включения или отключения политики и список всех допустимых размеров виртуальных машин, заданных в указанной политике.</span><span class="sxs-lookup"><span data-stu-id="48f02-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="48f02-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48f02-108">EXAMPLES</span></span>

## <span data-ttu-id="48f02-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48f02-109">PARAMETERS</span></span>

### <span data-ttu-id="48f02-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f02-110">-DefaultProfile</span></span>
<span data-ttu-id="48f02-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="48f02-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48f02-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="48f02-112">-LabName</span></span>
<span data-ttu-id="48f02-113">Указывает имя лаборатории, для которой этот командлет получает политику размера виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="48f02-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="48f02-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f02-114">-ResourceGroupName</span></span>
<span data-ttu-id="48f02-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="48f02-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f02-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f02-116">CommonParameters</span></span>
<span data-ttu-id="48f02-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48f02-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f02-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f02-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f02-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48f02-119">INPUTS</span></span>

### <span data-ttu-id="48f02-120">System. String</span><span class="sxs-lookup"><span data-stu-id="48f02-120">System.String</span></span>

## <span data-ttu-id="48f02-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48f02-121">OUTPUTS</span></span>

### <span data-ttu-id="48f02-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="48f02-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="48f02-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="48f02-123">NOTES</span></span>

## <span data-ttu-id="48f02-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48f02-124">RELATED LINKS</span></span>

[<span data-ttu-id="48f02-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="48f02-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="48f02-126">Командлеты лаборатории тестирования для разработчиков Azure</span><span class="sxs-lookup"><span data-stu-id="48f02-126">Azure Development Test Lab Cmdlets</span></span>](./Az.DevTestLabs.md)


