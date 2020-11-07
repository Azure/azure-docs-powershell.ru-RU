---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: cb28249d5c32119d187becd8b07f2137f3f312d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732117"
---
# <span data-ttu-id="1cf00-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="1cf00-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="1cf00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cf00-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf00-103">Удаление резервной копии с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1cf00-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cf00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cf00-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cf00-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cf00-105">DESCRIPTION</span></span>

## <span data-ttu-id="1cf00-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cf00-106">EXAMPLES</span></span>

### <span data-ttu-id="1cf00-107">1:</span><span class="sxs-lookup"><span data-stu-id="1cf00-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1cf00-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cf00-108">PARAMETERS</span></span>

### <span data-ttu-id="1cf00-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf00-109">-DefaultProfile</span></span>
<span data-ttu-id="1cf00-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf00-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf00-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf00-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1cf00-112">-Тег</span><span class="sxs-lookup"><span data-stu-id="1cf00-112">-Tag</span></span>
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

### <span data-ttu-id="1cf00-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="1cf00-113">-VMName</span></span>
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

### <span data-ttu-id="1cf00-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf00-114">CommonParameters</span></span>
<span data-ttu-id="1cf00-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cf00-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf00-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf00-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf00-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cf00-117">INPUTS</span></span>

### <span data-ttu-id="1cf00-118">System. String</span><span class="sxs-lookup"><span data-stu-id="1cf00-118">System.String</span></span>

## <span data-ttu-id="1cf00-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cf00-119">OUTPUTS</span></span>

### <span data-ttu-id="1cf00-120">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1cf00-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1cf00-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cf00-121">NOTES</span></span>

## <span data-ttu-id="1cf00-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cf00-122">RELATED LINKS</span></span>
