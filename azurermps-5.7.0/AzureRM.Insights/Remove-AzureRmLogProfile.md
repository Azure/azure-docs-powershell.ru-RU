---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561780"
---
# <span data-ttu-id="c14b8-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c14b8-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="c14b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c14b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c14b8-103">Удаление профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="c14b8-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c14b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c14b8-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c14b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c14b8-105">DESCRIPTION</span></span>
<span data-ttu-id="c14b8-106">Командлет **Remove-AzureRmLogProfile** удаляет профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="c14b8-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="c14b8-107">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="c14b8-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c14b8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c14b8-108">EXAMPLES</span></span>

## <span data-ttu-id="c14b8-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c14b8-109">PARAMETERS</span></span>

### <span data-ttu-id="c14b8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14b8-110">-DefaultProfile</span></span>
<span data-ttu-id="c14b8-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c14b8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c14b8-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c14b8-112">-Name</span></span>
<span data-ttu-id="c14b8-113">Указывает имя профиля, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c14b8-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14b8-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c14b8-114">-PassThru</span></span>
<span data-ttu-id="c14b8-115">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="c14b8-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14b8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14b8-116">CommonParameters</span></span>
<span data-ttu-id="c14b8-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c14b8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14b8-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14b8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14b8-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c14b8-119">INPUTS</span></span>

### <span data-ttu-id="c14b8-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="c14b8-120">None</span></span>
<span data-ttu-id="c14b8-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c14b8-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c14b8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c14b8-122">OUTPUTS</span></span>

### <span data-ttu-id="c14b8-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c14b8-123">AzureOperationResponse</span></span>

## <span data-ttu-id="c14b8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c14b8-124">NOTES</span></span>

## <span data-ttu-id="c14b8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c14b8-125">RELATED LINKS</span></span>

[<span data-ttu-id="c14b8-126">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c14b8-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="c14b8-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c14b8-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


