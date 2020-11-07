---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914518"
---
# <span data-ttu-id="d8d77-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="d8d77-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="d8d77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8d77-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d77-103">Удаление резервной копии с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d8d77-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8d77-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d77-105">DESCRIPTION</span></span>

## <span data-ttu-id="d8d77-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8d77-106">EXAMPLES</span></span>

### <span data-ttu-id="d8d77-107">1:</span><span class="sxs-lookup"><span data-stu-id="d8d77-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d8d77-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8d77-108">PARAMETERS</span></span>

### <span data-ttu-id="d8d77-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d77-109">-DefaultProfile</span></span>
<span data-ttu-id="d8d77-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d77-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8d77-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d77-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d8d77-112">-Тег</span><span class="sxs-lookup"><span data-stu-id="d8d77-112">-Tag</span></span>
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

### <span data-ttu-id="d8d77-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="d8d77-113">-VMName</span></span>
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

### <span data-ttu-id="d8d77-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d77-114">CommonParameters</span></span>
<span data-ttu-id="d8d77-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8d77-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d77-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d77-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d77-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8d77-117">INPUTS</span></span>

### <span data-ttu-id="d8d77-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="d8d77-118">None</span></span>
<span data-ttu-id="d8d77-119">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d8d77-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8d77-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d77-120">OUTPUTS</span></span>

### <span data-ttu-id="d8d77-121">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d8d77-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d8d77-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8d77-122">NOTES</span></span>

## <span data-ttu-id="d8d77-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8d77-123">RELATED LINKS</span></span>

