---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412967"
---
# <span data-ttu-id="e1d30-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="e1d30-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="e1d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d30-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d30-103">Удаляет резервную копию с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e1d30-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="e1d30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1d30-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d30-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d30-105">DESCRIPTION</span></span>

## <span data-ttu-id="e1d30-106">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1d30-106">EXAMPLES</span></span>

### <span data-ttu-id="e1d30-107">1:</span><span class="sxs-lookup"><span data-stu-id="e1d30-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e1d30-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d30-108">PARAMETERS</span></span>

### <span data-ttu-id="e1d30-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d30-109">-DefaultProfile</span></span>
<span data-ttu-id="e1d30-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d30-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d30-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d30-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e1d30-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1d30-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="e1d30-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d30-114">CommonParameters</span></span>
<span data-ttu-id="e1d30-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d30-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d30-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1d30-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d30-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1d30-117">INPUTS</span></span>

### <span data-ttu-id="e1d30-118">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d30-118">System.String</span></span>

## <span data-ttu-id="e1d30-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1d30-119">OUTPUTS</span></span>

### <span data-ttu-id="e1d30-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e1d30-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e1d30-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1d30-121">NOTES</span></span>

## <span data-ttu-id="e1d30-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1d30-122">RELATED LINKS</span></span>
