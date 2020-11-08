---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242751"
---
# <span data-ttu-id="69e1c-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="69e1c-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="69e1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="69e1c-103">Возвращает ключи BitLocker для всех дисков в указанном задании.</span><span class="sxs-lookup"><span data-stu-id="69e1c-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="69e1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69e1c-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="69e1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="69e1c-106">Возвращает ключи BitLocker для всех дисков в указанном задании.</span><span class="sxs-lookup"><span data-stu-id="69e1c-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="69e1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69e1c-107">EXAMPLES</span></span>

### <span data-ttu-id="69e1c-108">Пример 1: список всех ключей BitLocker в указанном задании ImportExport</span><span class="sxs-lookup"><span data-stu-id="69e1c-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="69e1c-109">Этот командлет перечисляет все ключи BitLocker в указанном задании ImportExport.</span><span class="sxs-lookup"><span data-stu-id="69e1c-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="69e1c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69e1c-110">PARAMETERS</span></span>

### <span data-ttu-id="69e1c-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="69e1c-111">-AcceptLanguage</span></span>
<span data-ttu-id="69e1c-112">Указывает предпочтительный язык ответа.</span><span class="sxs-lookup"><span data-stu-id="69e1c-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="69e1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e1c-113">-DefaultProfile</span></span>
<span data-ttu-id="69e1c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69e1c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69e1c-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="69e1c-115">-JobName</span></span>
<span data-ttu-id="69e1c-116">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="69e1c-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="69e1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="69e1c-118">Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="69e1c-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="69e1c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69e1c-119">-SubscriptionId</span></span>
<span data-ttu-id="69e1c-120">Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="69e1c-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="69e1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e1c-121">CommonParameters</span></span>
<span data-ttu-id="69e1c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69e1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e1c-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69e1c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e1c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69e1c-124">INPUTS</span></span>

## <span data-ttu-id="69e1c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69e1c-125">OUTPUTS</span></span>

### <span data-ttu-id="69e1c-126">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="69e1c-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="69e1c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="69e1c-127">NOTES</span></span>

<span data-ttu-id="69e1c-128">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="69e1c-128">ALIASES</span></span>

## <span data-ttu-id="69e1c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69e1c-129">RELATED LINKS</span></span>

