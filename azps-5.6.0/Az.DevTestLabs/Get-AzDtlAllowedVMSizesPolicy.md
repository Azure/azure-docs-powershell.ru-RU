---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: f1b5d95397aad24b84462c7e9ceba4a06ba854c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994356"
---
# <span data-ttu-id="bb23c-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="bb23c-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="bb23c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb23c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb23c-103">Получает политику разрешенных размеров виртуальных машин в лабораторной лаборатории DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="bb23c-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="bb23c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb23c-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb23c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb23c-105">DESCRIPTION</span></span>
<span data-ttu-id="bb23c-106">Для **cmdlet Get-AzDtlAllowedVMSizesPolicy** замеряется политика допустимого размера виртуальных машин, которая позволяет указать список допустимого размера виртуальной машины в лабораторных условиях.</span><span class="sxs-lookup"><span data-stu-id="bb23c-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="bb23c-107">Он возвращает состояние политики (включена или отключена) и список всех разрешенных размеров виртуальных машин, установленных в указанной политике.</span><span class="sxs-lookup"><span data-stu-id="bb23c-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="bb23c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb23c-108">EXAMPLES</span></span>

## <span data-ttu-id="bb23c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb23c-109">PARAMETERS</span></span>

### <span data-ttu-id="bb23c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb23c-110">-DefaultProfile</span></span>
<span data-ttu-id="bb23c-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb23c-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb23c-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="bb23c-112">-LabName</span></span>
<span data-ttu-id="bb23c-113">Указывает имя лаборатории, для которой этот cmdlet получает политику размера виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="bb23c-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="bb23c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb23c-114">-ResourceGroupName</span></span>
<span data-ttu-id="bb23c-115">Имя группы ресурсов, к которой относится лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="bb23c-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="bb23c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb23c-116">CommonParameters</span></span>
<span data-ttu-id="bb23c-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb23c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb23c-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb23c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb23c-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb23c-119">INPUTS</span></span>

### <span data-ttu-id="bb23c-120">System.String</span><span class="sxs-lookup"><span data-stu-id="bb23c-120">System.String</span></span>

## <span data-ttu-id="bb23c-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb23c-121">OUTPUTS</span></span>

### <span data-ttu-id="bb23c-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="bb23c-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="bb23c-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb23c-123">NOTES</span></span>

## <span data-ttu-id="bb23c-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb23c-124">RELATED LINKS</span></span>

[<span data-ttu-id="bb23c-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="bb23c-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


