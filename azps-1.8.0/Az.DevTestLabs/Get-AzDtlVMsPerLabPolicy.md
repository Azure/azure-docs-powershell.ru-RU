---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 2603a9c5f259de05b466693bdc42d7a6dfb2eda2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730948"
---
# <span data-ttu-id="dbd02-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="dbd02-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="dbd02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dbd02-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd02-103">Получает виртуальные машины для каждой политики лаборатории лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="dbd02-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="dbd02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dbd02-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbd02-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd02-106">Командлет **Get-AzDtlVMsPerLabPolicy** получает виртуальные машины для каждой политики лаборатории лаборатории, которая позволяет задавать общее количество виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="dbd02-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="dbd02-107">Командлет возвращает состояние политики "включено" или "отключено", а также общее количество разрешенных виртуальных машин в лаборатории, заданной в политике.</span><span class="sxs-lookup"><span data-stu-id="dbd02-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="dbd02-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dbd02-108">EXAMPLES</span></span>

## <span data-ttu-id="dbd02-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dbd02-109">PARAMETERS</span></span>

### <span data-ttu-id="dbd02-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd02-110">-DefaultProfile</span></span>
<span data-ttu-id="dbd02-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dbd02-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbd02-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="dbd02-112">-LabName</span></span>
<span data-ttu-id="dbd02-113">Указывает имя лаборатории, для которой этот командлет получает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="dbd02-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="dbd02-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd02-114">-ResourceGroupName</span></span>
<span data-ttu-id="dbd02-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="dbd02-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="dbd02-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd02-116">CommonParameters</span></span>
<span data-ttu-id="dbd02-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dbd02-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd02-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd02-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd02-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dbd02-119">INPUTS</span></span>

### <span data-ttu-id="dbd02-120">System. String</span><span class="sxs-lookup"><span data-stu-id="dbd02-120">System.String</span></span>

## <span data-ttu-id="dbd02-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbd02-121">OUTPUTS</span></span>

### <span data-ttu-id="dbd02-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="dbd02-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="dbd02-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="dbd02-123">NOTES</span></span>

## <span data-ttu-id="dbd02-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbd02-124">RELATED LINKS</span></span>

[<span data-ttu-id="dbd02-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="dbd02-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


