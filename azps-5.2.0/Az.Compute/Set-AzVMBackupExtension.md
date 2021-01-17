---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398047"
---
# <span data-ttu-id="504e9-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="504e9-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="504e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504e9-102">SYNOPSIS</span></span>
<span data-ttu-id="504e9-103">Задает свойства расширения резервной копии на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="504e9-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="504e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="504e9-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="504e9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="504e9-105">DESCRIPTION</span></span>

## <span data-ttu-id="504e9-106">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="504e9-106">EXAMPLES</span></span>

### <span data-ttu-id="504e9-107">1:</span><span class="sxs-lookup"><span data-stu-id="504e9-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="504e9-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="504e9-108">PARAMETERS</span></span>

### <span data-ttu-id="504e9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504e9-109">-DefaultProfile</span></span>
<span data-ttu-id="504e9-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="504e9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="504e9-111">-Name</span><span class="sxs-lookup"><span data-stu-id="504e9-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504e9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="504e9-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="504e9-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="504e9-113">-Tag</span></span>
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

### <span data-ttu-id="504e9-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="504e9-114">-VMName</span></span>
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

### <span data-ttu-id="504e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504e9-115">CommonParameters</span></span>
<span data-ttu-id="504e9-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="504e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504e9-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="504e9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504e9-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="504e9-118">INPUTS</span></span>

### <span data-ttu-id="504e9-119">System.String</span><span class="sxs-lookup"><span data-stu-id="504e9-119">System.String</span></span>

## <span data-ttu-id="504e9-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="504e9-120">OUTPUTS</span></span>

### <span data-ttu-id="504e9-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="504e9-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="504e9-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="504e9-122">NOTES</span></span>

## <span data-ttu-id="504e9-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="504e9-123">RELATED LINKS</span></span>
