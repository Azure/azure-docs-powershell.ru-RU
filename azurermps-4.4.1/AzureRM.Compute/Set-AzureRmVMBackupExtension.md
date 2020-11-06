---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: d95ef152ed21439aafdc1cf9778b101473539b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557819"
---
# <span data-ttu-id="ceca9-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="ceca9-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="ceca9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ceca9-102">SYNOPSIS</span></span>
<span data-ttu-id="ceca9-103">Задает свойства модуля резервного копирования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ceca9-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceca9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ceca9-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceca9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceca9-105">DESCRIPTION</span></span>

## <span data-ttu-id="ceca9-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ceca9-106">EXAMPLES</span></span>

### <span data-ttu-id="ceca9-107">1:</span><span class="sxs-lookup"><span data-stu-id="ceca9-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ceca9-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ceca9-108">PARAMETERS</span></span>

### <span data-ttu-id="ceca9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceca9-109">-DefaultProfile</span></span>
<span data-ttu-id="ceca9-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceca9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceca9-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ceca9-111">-Name</span></span>
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

### <span data-ttu-id="ceca9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceca9-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ceca9-113">-Тег</span><span class="sxs-lookup"><span data-stu-id="ceca9-113">-Tag</span></span>
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

### <span data-ttu-id="ceca9-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="ceca9-114">-VMName</span></span>
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

### <span data-ttu-id="ceca9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceca9-115">CommonParameters</span></span>
<span data-ttu-id="ceca9-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ceca9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceca9-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceca9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceca9-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ceca9-118">INPUTS</span></span>

## <span data-ttu-id="ceca9-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceca9-119">OUTPUTS</span></span>

## <span data-ttu-id="ceca9-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="ceca9-120">NOTES</span></span>

## <span data-ttu-id="ceca9-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceca9-121">RELATED LINKS</span></span>

