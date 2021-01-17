---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398471"
---
# <span data-ttu-id="f9742-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="f9742-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="f9742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9742-102">SYNOPSIS</span></span>
<span data-ttu-id="f9742-103">Получает виртуальные машины на пользователя в лабораторной лаборатории DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="f9742-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="f9742-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f9742-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9742-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9742-105">DESCRIPTION</span></span>
<span data-ttu-id="f9742-106">Cmdlet **Get-AzDtlVMsPerUserPolicy** получает виртуальные машины на пользователя в лабораторных условиях, что позволяет установить максимальное количество виртуальных машин, разрешенных для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f9742-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="f9742-107">Он возвращает состояние политики (включена или отключена), а также максимальное количество виртуальных машин, разрешенных пользователем, за которое она настроена.</span><span class="sxs-lookup"><span data-stu-id="f9742-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="f9742-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f9742-108">EXAMPLES</span></span>

## <span data-ttu-id="f9742-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9742-109">PARAMETERS</span></span>

### <span data-ttu-id="f9742-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9742-110">-DefaultProfile</span></span>
<span data-ttu-id="f9742-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f9742-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9742-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="f9742-112">-LabName</span></span>
<span data-ttu-id="f9742-113">Указывает имя лабораторных, для которых этот cmdlet получает виртуальную машину для политики пользователя.</span><span class="sxs-lookup"><span data-stu-id="f9742-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="f9742-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9742-114">-ResourceGroupName</span></span>
<span data-ttu-id="f9742-115">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="f9742-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="f9742-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9742-116">CommonParameters</span></span>
<span data-ttu-id="f9742-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9742-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9742-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9742-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9742-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9742-119">INPUTS</span></span>

### <span data-ttu-id="f9742-120">System.String</span><span class="sxs-lookup"><span data-stu-id="f9742-120">System.String</span></span>

## <span data-ttu-id="f9742-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f9742-121">OUTPUTS</span></span>

### <span data-ttu-id="f9742-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f9742-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="f9742-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f9742-123">NOTES</span></span>

## <span data-ttu-id="f9742-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9742-124">RELATED LINKS</span></span>

[<span data-ttu-id="f9742-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="f9742-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


