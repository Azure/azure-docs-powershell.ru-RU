---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 1c2b58d58303dba38f907e9019f45502218c345a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721774"
---
# <span data-ttu-id="e8f41-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="e8f41-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="e8f41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8f41-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f41-103">Удаление резервной копии с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8f41-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="e8f41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8f41-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8f41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f41-105">DESCRIPTION</span></span>

## <span data-ttu-id="e8f41-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8f41-106">EXAMPLES</span></span>

### <span data-ttu-id="e8f41-107">1:</span><span class="sxs-lookup"><span data-stu-id="e8f41-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e8f41-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8f41-108">PARAMETERS</span></span>

### <span data-ttu-id="e8f41-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f41-109">-DefaultProfile</span></span>
<span data-ttu-id="e8f41-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f41-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8f41-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f41-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e8f41-112">-Тег</span><span class="sxs-lookup"><span data-stu-id="e8f41-112">-Tag</span></span>
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

### <span data-ttu-id="e8f41-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="e8f41-113">-VMName</span></span>
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

### <span data-ttu-id="e8f41-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f41-114">CommonParameters</span></span>
<span data-ttu-id="e8f41-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8f41-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f41-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8f41-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f41-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8f41-117">INPUTS</span></span>

### <span data-ttu-id="e8f41-118">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f41-118">System.String</span></span>

## <span data-ttu-id="e8f41-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f41-119">OUTPUTS</span></span>

### <span data-ttu-id="e8f41-120">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e8f41-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e8f41-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8f41-121">NOTES</span></span>

## <span data-ttu-id="e8f41-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8f41-122">RELATED LINKS</span></span>
