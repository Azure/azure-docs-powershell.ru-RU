---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911425"
---
# <span data-ttu-id="12933-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="12933-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="12933-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12933-102">SYNOPSIS</span></span>
<span data-ttu-id="12933-103">Удаление резервной копии с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="12933-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="12933-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12933-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12933-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12933-105">DESCRIPTION</span></span>

## <span data-ttu-id="12933-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12933-106">EXAMPLES</span></span>

### <span data-ttu-id="12933-107">1:</span><span class="sxs-lookup"><span data-stu-id="12933-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="12933-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12933-108">PARAMETERS</span></span>

### <span data-ttu-id="12933-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12933-109">-DefaultProfile</span></span>
<span data-ttu-id="12933-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12933-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12933-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12933-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12933-112">-Тег</span><span class="sxs-lookup"><span data-stu-id="12933-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12933-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="12933-113">-VMName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12933-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12933-114">CommonParameters</span></span>
<span data-ttu-id="12933-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12933-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12933-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12933-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12933-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12933-117">INPUTS</span></span>

### <span data-ttu-id="12933-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="12933-118">None</span></span>
<span data-ttu-id="12933-119">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="12933-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12933-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12933-120">OUTPUTS</span></span>

### <span data-ttu-id="12933-121">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="12933-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="12933-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="12933-122">NOTES</span></span>

## <span data-ttu-id="12933-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12933-123">RELATED LINKS</span></span>

