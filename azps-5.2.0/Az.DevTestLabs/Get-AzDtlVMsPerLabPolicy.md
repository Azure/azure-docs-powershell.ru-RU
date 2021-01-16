---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328834"
---
# <span data-ttu-id="36030-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="36030-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="36030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36030-102">SYNOPSIS</span></span>
<span data-ttu-id="36030-103">Получает виртуальные машины на каждый лабораторный анализ в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="36030-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="36030-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36030-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36030-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36030-105">DESCRIPTION</span></span>
<span data-ttu-id="36030-106">Для **этого** используется политика виртуальной машины для лабораторной работы, которая позволяет установить общее количество виртуальных машин, разрешенных в этой лабораторной.</span><span class="sxs-lookup"><span data-stu-id="36030-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="36030-107">Он возвращает состояние политики (включена или отключена), а также общее количество виртуальных машин, разрешенных в задаемой в политике лабораторной.</span><span class="sxs-lookup"><span data-stu-id="36030-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="36030-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36030-108">EXAMPLES</span></span>

## <span data-ttu-id="36030-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36030-109">PARAMETERS</span></span>

### <span data-ttu-id="36030-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36030-110">-DefaultProfile</span></span>
<span data-ttu-id="36030-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36030-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36030-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="36030-112">-LabName</span></span>
<span data-ttu-id="36030-113">Указывает имя лабораторных буклетов, для которых этот cmdlet получает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="36030-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="36030-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36030-114">-ResourceGroupName</span></span>
<span data-ttu-id="36030-115">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="36030-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="36030-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36030-116">CommonParameters</span></span>
<span data-ttu-id="36030-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36030-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36030-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36030-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36030-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36030-119">INPUTS</span></span>

### <span data-ttu-id="36030-120">System.String</span><span class="sxs-lookup"><span data-stu-id="36030-120">System.String</span></span>

## <span data-ttu-id="36030-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36030-121">OUTPUTS</span></span>

### <span data-ttu-id="36030-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="36030-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="36030-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36030-123">NOTES</span></span>

## <span data-ttu-id="36030-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36030-124">RELATED LINKS</span></span>

[<span data-ttu-id="36030-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="36030-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


