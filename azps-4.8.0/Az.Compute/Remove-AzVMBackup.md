---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078403"
---
# <span data-ttu-id="5c5ec-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="5c5ec-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="5c5ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5ec-103">Удаление резервной копии с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="5c5ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c5ec-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c5ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c5ec-105">DESCRIPTION</span></span>

## <span data-ttu-id="5c5ec-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c5ec-106">EXAMPLES</span></span>

### <span data-ttu-id="5c5ec-107">1:</span><span class="sxs-lookup"><span data-stu-id="5c5ec-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="5c5ec-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c5ec-108">PARAMETERS</span></span>

### <span data-ttu-id="5c5ec-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5ec-109">-DefaultProfile</span></span>
<span data-ttu-id="5c5ec-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c5ec-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5ec-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5c5ec-112">-Тег</span><span class="sxs-lookup"><span data-stu-id="5c5ec-112">-Tag</span></span>
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

### <span data-ttu-id="5c5ec-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="5c5ec-113">-VMName</span></span>
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

### <span data-ttu-id="5c5ec-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5ec-114">CommonParameters</span></span>
<span data-ttu-id="5c5ec-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5ec-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c5ec-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5ec-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c5ec-117">INPUTS</span></span>

### <span data-ttu-id="5c5ec-118">System. String</span><span class="sxs-lookup"><span data-stu-id="5c5ec-118">System.String</span></span>

## <span data-ttu-id="5c5ec-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c5ec-119">OUTPUTS</span></span>

### <span data-ttu-id="5c5ec-120">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5c5ec-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5c5ec-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c5ec-121">NOTES</span></span>

## <span data-ttu-id="5c5ec-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c5ec-122">RELATED LINKS</span></span>