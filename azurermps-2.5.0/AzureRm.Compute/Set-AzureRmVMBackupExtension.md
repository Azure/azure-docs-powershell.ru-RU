---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914150"
---
# <span data-ttu-id="828e2-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="828e2-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="828e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="828e2-102">SYNOPSIS</span></span>
<span data-ttu-id="828e2-103">Задает свойства модуля резервного копирования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="828e2-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="828e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="828e2-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="828e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="828e2-105">DESCRIPTION</span></span>

## <span data-ttu-id="828e2-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="828e2-106">EXAMPLES</span></span>

### <span data-ttu-id="828e2-107">1:</span><span class="sxs-lookup"><span data-stu-id="828e2-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="828e2-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="828e2-108">PARAMETERS</span></span>

### <span data-ttu-id="828e2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828e2-109">-DefaultProfile</span></span>
<span data-ttu-id="828e2-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="828e2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="828e2-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="828e2-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828e2-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828e2-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="828e2-113">-Тег</span><span class="sxs-lookup"><span data-stu-id="828e2-113">-Tag</span></span>
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

### <span data-ttu-id="828e2-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="828e2-114">-VMName</span></span>
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

### <span data-ttu-id="828e2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828e2-115">CommonParameters</span></span>
<span data-ttu-id="828e2-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="828e2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828e2-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828e2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828e2-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="828e2-118">INPUTS</span></span>

### <span data-ttu-id="828e2-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="828e2-119">None</span></span>
<span data-ttu-id="828e2-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="828e2-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="828e2-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="828e2-121">OUTPUTS</span></span>

### <span data-ttu-id="828e2-122">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="828e2-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="828e2-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="828e2-123">NOTES</span></span>

## <span data-ttu-id="828e2-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="828e2-124">RELATED LINKS</span></span>

