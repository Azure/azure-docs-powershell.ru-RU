---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: f931f0ffb38af251be3ffb213b61f7033bb59150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733369"
---
# <span data-ttu-id="fb307-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="fb307-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="fb307-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb307-102">SYNOPSIS</span></span>
<span data-ttu-id="fb307-103">Удаление профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="fb307-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb307-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb307-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb307-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb307-105">DESCRIPTION</span></span>
<span data-ttu-id="fb307-106">Командлет **Remove-AzureRmLogProfile** удаляет профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="fb307-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

## <span data-ttu-id="fb307-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb307-107">EXAMPLES</span></span>

## <span data-ttu-id="fb307-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb307-108">PARAMETERS</span></span>

### <span data-ttu-id="fb307-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb307-109">-Name</span></span>
<span data-ttu-id="fb307-110">Указывает имя профиля, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fb307-110">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb307-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb307-111">-DefaultProfile</span></span>
<span data-ttu-id="fb307-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb307-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb307-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb307-113">-PassThru</span></span>
<span data-ttu-id="fb307-114">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="fb307-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb307-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb307-115">CommonParameters</span></span>
<span data-ttu-id="fb307-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb307-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb307-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb307-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb307-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb307-118">INPUTS</span></span>

## <span data-ttu-id="fb307-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb307-119">OUTPUTS</span></span>

### <span data-ttu-id="fb307-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb307-120">System.Boolean</span></span>

## <span data-ttu-id="fb307-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb307-121">NOTES</span></span>

## <span data-ttu-id="fb307-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb307-122">RELATED LINKS</span></span>

[<span data-ttu-id="fb307-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="fb307-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="fb307-124">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="fb307-124">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


