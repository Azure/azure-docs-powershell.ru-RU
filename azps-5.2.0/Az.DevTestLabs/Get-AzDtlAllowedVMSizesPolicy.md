---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396703"
---
# <span data-ttu-id="02cad-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="02cad-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="02cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02cad-102">SYNOPSIS</span></span>
<span data-ttu-id="02cad-103">Получает политику разрешенных размеров виртуальных машин в лабораторной лаборатории DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="02cad-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="02cad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02cad-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02cad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02cad-105">DESCRIPTION</span></span>
<span data-ttu-id="02cad-106">Для **cmdlet Get-AzDtlAllowedVMSizesPolicy** замеряется политика допустимого размера виртуальных машин, которая позволяет указать список допустимого размера виртуальной машины в лабораторных условиях.</span><span class="sxs-lookup"><span data-stu-id="02cad-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="02cad-107">Он возвращает состояние политики (включена или отключена) и список всех разрешенных размеров виртуальных машин, установленных в указанной политике.</span><span class="sxs-lookup"><span data-stu-id="02cad-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="02cad-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02cad-108">EXAMPLES</span></span>

## <span data-ttu-id="02cad-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02cad-109">PARAMETERS</span></span>

### <span data-ttu-id="02cad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02cad-110">-DefaultProfile</span></span>
<span data-ttu-id="02cad-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="02cad-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02cad-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="02cad-112">-LabName</span></span>
<span data-ttu-id="02cad-113">Указывает имя лабораторных, для которых этот cmdlet получает политику размера виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="02cad-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="02cad-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02cad-114">-ResourceGroupName</span></span>
<span data-ttu-id="02cad-115">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="02cad-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="02cad-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02cad-116">CommonParameters</span></span>
<span data-ttu-id="02cad-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02cad-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02cad-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02cad-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02cad-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02cad-119">INPUTS</span></span>

### <span data-ttu-id="02cad-120">System.String</span><span class="sxs-lookup"><span data-stu-id="02cad-120">System.String</span></span>

## <span data-ttu-id="02cad-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02cad-121">OUTPUTS</span></span>

### <span data-ttu-id="02cad-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="02cad-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="02cad-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02cad-123">NOTES</span></span>

## <span data-ttu-id="02cad-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02cad-124">RELATED LINKS</span></span>

[<span data-ttu-id="02cad-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="02cad-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


