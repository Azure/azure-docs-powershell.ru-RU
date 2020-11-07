---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: 194fcfddef0d85925bc08fb53fa7f5acf860e9ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912369"
---
# <span data-ttu-id="f1b89-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="f1b89-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="f1b89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1b89-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b89-103">Получение сведений о параметрах синхронизации для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f1b89-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="f1b89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1b89-104">SYNTAX</span></span>

### <span data-ttu-id="f1b89-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1b89-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1b89-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1b89-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1b89-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1b89-107">DESCRIPTION</span></span>
<span data-ttu-id="f1b89-108">Командлет **Get-AzDataShareSynchronization** содержит сведения обо всех параметрах синхронизации, указанных в общем доступе в учетной записи для общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="f1b89-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="f1b89-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1b89-109">EXAMPLES</span></span>

### <span data-ttu-id="f1b89-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1b89-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="f1b89-111">Эти команды предоставляют сведения обо всех параметрах синхронизации, представленных в AdsShare для общего доступа к данным в WikiAds учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1b89-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="f1b89-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1b89-112">PARAMETERS</span></span>

### <span data-ttu-id="f1b89-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f1b89-113">-AccountName</span></span>
<span data-ttu-id="f1b89-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="f1b89-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b89-115">-DefaultProfile</span></span>
<span data-ttu-id="f1b89-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b89-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b89-117">-ResourceGroupName</span></span>
<span data-ttu-id="f1b89-118">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="f1b89-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b89-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1b89-119">-ResourceId</span></span>
<span data-ttu-id="f1b89-120">Идентификатор ресурса "общий доступ к данным Azure"</span><span class="sxs-lookup"><span data-stu-id="f1b89-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b89-121">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="f1b89-121">-ShareName</span></span>
<span data-ttu-id="f1b89-122">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="f1b89-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b89-123">CommonParameters</span></span>
<span data-ttu-id="f1b89-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1b89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b89-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b89-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b89-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1b89-126">INPUTS</span></span>

### <span data-ttu-id="f1b89-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f1b89-127">System.String</span></span>

## <span data-ttu-id="f1b89-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1b89-128">OUTPUTS</span></span>

### <span data-ttu-id="f1b89-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="f1b89-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="f1b89-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1b89-130">NOTES</span></span>

## <span data-ttu-id="f1b89-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1b89-131">RELATED LINKS</span></span>
