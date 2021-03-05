---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: fefd529b00b88c20b3703e1bcecbbb88c72d52e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963000"
---
# <span data-ttu-id="c5f86-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="c5f86-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="c5f86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f86-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f86-103">Возвращает ключи BitLocker для всех дисков в указанном задание.</span><span class="sxs-lookup"><span data-stu-id="c5f86-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="c5f86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5f86-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c5f86-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5f86-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f86-106">Возвращает ключи BitLocker для всех дисков в указанном задание.</span><span class="sxs-lookup"><span data-stu-id="c5f86-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="c5f86-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5f86-107">EXAMPLES</span></span>

### <span data-ttu-id="c5f86-108">Пример 1. Список всех ключей BitLocker в указанном задание ImportExport</span><span class="sxs-lookup"><span data-stu-id="c5f86-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="c5f86-109">Этот cmdlet lists all BitLocker Keys in specified ImportExport job.</span><span class="sxs-lookup"><span data-stu-id="c5f86-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="c5f86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5f86-110">PARAMETERS</span></span>

### <span data-ttu-id="c5f86-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="c5f86-111">-AcceptLanguage</span></span>
<span data-ttu-id="c5f86-112">Указывает предпочтительный язык для ответа.</span><span class="sxs-lookup"><span data-stu-id="c5f86-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f86-113">-DefaultProfile</span></span>
<span data-ttu-id="c5f86-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f86-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f86-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="c5f86-115">-JobName</span></span>
<span data-ttu-id="c5f86-116">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="c5f86-116">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f86-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5f86-118">Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="c5f86-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f86-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5f86-119">-SubscriptionId</span></span>
<span data-ttu-id="c5f86-120">ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f86-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f86-121">CommonParameters</span></span>
<span data-ttu-id="c5f86-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f86-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5f86-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f86-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5f86-124">INPUTS</span></span>

## <span data-ttu-id="c5f86-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5f86-125">OUTPUTS</span></span>

### <span data-ttu-id="c5f86-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="c5f86-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="c5f86-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5f86-127">NOTES</span></span>

<span data-ttu-id="c5f86-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c5f86-128">ALIASES</span></span>

## <span data-ttu-id="c5f86-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5f86-129">RELATED LINKS</span></span>

