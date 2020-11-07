---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911350"
---
# <span data-ttu-id="5e30e-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="5e30e-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="5e30e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e30e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e30e-103">Задает свойства модуля резервного копирования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5e30e-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="5e30e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e30e-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e30e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e30e-105">DESCRIPTION</span></span>

## <span data-ttu-id="5e30e-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e30e-106">EXAMPLES</span></span>

### <span data-ttu-id="5e30e-107">1:</span><span class="sxs-lookup"><span data-stu-id="5e30e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="5e30e-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e30e-108">PARAMETERS</span></span>

### <span data-ttu-id="5e30e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e30e-109">-DefaultProfile</span></span>
<span data-ttu-id="5e30e-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e30e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e30e-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e30e-111">-Name</span></span>
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

### <span data-ttu-id="5e30e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e30e-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5e30e-113">-Тег</span><span class="sxs-lookup"><span data-stu-id="5e30e-113">-Tag</span></span>
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

### <span data-ttu-id="5e30e-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="5e30e-114">-VMName</span></span>
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

### <span data-ttu-id="5e30e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e30e-115">CommonParameters</span></span>
<span data-ttu-id="5e30e-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e30e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e30e-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e30e-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e30e-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e30e-118">INPUTS</span></span>

### <span data-ttu-id="5e30e-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="5e30e-119">None</span></span>
<span data-ttu-id="5e30e-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5e30e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e30e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e30e-121">OUTPUTS</span></span>

### <span data-ttu-id="5e30e-122">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5e30e-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5e30e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e30e-123">NOTES</span></span>

## <span data-ttu-id="5e30e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e30e-124">RELATED LINKS</span></span>

