---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245547"
---
# <span data-ttu-id="b71ed-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="b71ed-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="b71ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b71ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b71ed-103">Возвращает политику виртуальных машин на пользователя лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="b71ed-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="b71ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b71ed-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b71ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b71ed-105">DESCRIPTION</span></span>
<span data-ttu-id="b71ed-106">Командлет **Get-AzDtlVMsPerUserPolicy** получает виртуальные машины для пользовательской политики лаборатории, которая позволяет установить максимальное количество виртуальных машин, разрешенных для одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b71ed-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="b71ed-107">Командлет возвращает состояние политики "включено" или "отключено", а также максимальное количество виртуальных машин, разрешенных для одного пользователя, установленного в политике.</span><span class="sxs-lookup"><span data-stu-id="b71ed-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="b71ed-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b71ed-108">EXAMPLES</span></span>

## <span data-ttu-id="b71ed-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b71ed-109">PARAMETERS</span></span>

### <span data-ttu-id="b71ed-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71ed-110">-DefaultProfile</span></span>
<span data-ttu-id="b71ed-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b71ed-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b71ed-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b71ed-112">-LabName</span></span>
<span data-ttu-id="b71ed-113">Указывает имя лаборатории, для которой этот командлет получает политику виртуальной машины на пользователя.</span><span class="sxs-lookup"><span data-stu-id="b71ed-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="b71ed-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71ed-114">-ResourceGroupName</span></span>
<span data-ttu-id="b71ed-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="b71ed-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b71ed-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71ed-116">CommonParameters</span></span>
<span data-ttu-id="b71ed-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b71ed-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71ed-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b71ed-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71ed-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b71ed-119">INPUTS</span></span>

### <span data-ttu-id="b71ed-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b71ed-120">System.String</span></span>

## <span data-ttu-id="b71ed-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b71ed-121">OUTPUTS</span></span>

### <span data-ttu-id="b71ed-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b71ed-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="b71ed-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="b71ed-123">NOTES</span></span>

## <span data-ttu-id="b71ed-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b71ed-124">RELATED LINKS</span></span>

[<span data-ttu-id="b71ed-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="b71ed-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)

