---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234505"
---
# <span data-ttu-id="592f4-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="592f4-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="592f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="592f4-102">SYNOPSIS</span></span>
<span data-ttu-id="592f4-103">Получает виртуальные машины на пользователя в лабораторной лаборатории DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="592f4-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="592f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="592f4-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="592f4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="592f4-105">DESCRIPTION</span></span>
<span data-ttu-id="592f4-106">Cmdlet **Get-AzDtlVMsPerUserPolicy** получает виртуальные машины на пользователя в лабораторных условиях, что позволяет установить максимальное количество виртуальных машин, разрешенных для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="592f4-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="592f4-107">Он возвращает состояние политики (включена или отключена), а также максимальное количество виртуальных машин, разрешенных пользователем, за которое она настроена.</span><span class="sxs-lookup"><span data-stu-id="592f4-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="592f4-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="592f4-108">EXAMPLES</span></span>

## <span data-ttu-id="592f4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="592f4-109">PARAMETERS</span></span>

### <span data-ttu-id="592f4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592f4-110">-DefaultProfile</span></span>
<span data-ttu-id="592f4-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="592f4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="592f4-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="592f4-112">-LabName</span></span>
<span data-ttu-id="592f4-113">Указывает имя лаборатории, для которой этот cmdlet получает виртуальную машину для политики пользователя.</span><span class="sxs-lookup"><span data-stu-id="592f4-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="592f4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592f4-114">-ResourceGroupName</span></span>
<span data-ttu-id="592f4-115">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="592f4-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="592f4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592f4-116">CommonParameters</span></span>
<span data-ttu-id="592f4-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592f4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592f4-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="592f4-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592f4-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="592f4-119">INPUTS</span></span>

### <span data-ttu-id="592f4-120">System.String</span><span class="sxs-lookup"><span data-stu-id="592f4-120">System.String</span></span>

## <span data-ttu-id="592f4-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="592f4-121">OUTPUTS</span></span>

### <span data-ttu-id="592f4-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="592f4-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="592f4-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="592f4-123">NOTES</span></span>

## <span data-ttu-id="592f4-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="592f4-124">RELATED LINKS</span></span>

[<span data-ttu-id="592f4-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="592f4-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


