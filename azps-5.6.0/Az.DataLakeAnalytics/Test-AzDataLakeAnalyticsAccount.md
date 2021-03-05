---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b5c1303625676006929a3c2eee80f5d5961bc438
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009160"
---
# <span data-ttu-id="fd110-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fd110-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="fd110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd110-102">SYNOPSIS</span></span>
<span data-ttu-id="fd110-103">Проверяет наличие учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fd110-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="fd110-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd110-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd110-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd110-105">DESCRIPTION</span></span>
<span data-ttu-id="fd110-106">**Cmdlet Test-AzDataLakeAnalyticsAccount** проверяет наличие учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fd110-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="fd110-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd110-107">EXAMPLES</span></span>

### <span data-ttu-id="fd110-108">Пример 1. Проверка на существования учетной записи</span><span class="sxs-lookup"><span data-stu-id="fd110-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="fd110-109">Эта команда проверяет, существует ли учетная запись с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="fd110-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="fd110-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd110-110">PARAMETERS</span></span>

### <span data-ttu-id="fd110-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd110-111">-DefaultProfile</span></span>
<span data-ttu-id="fd110-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fd110-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd110-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fd110-113">-Name</span></span>
<span data-ttu-id="fd110-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fd110-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="fd110-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd110-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd110-116">Имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fd110-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd110-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd110-117">CommonParameters</span></span>
<span data-ttu-id="fd110-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd110-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd110-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd110-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd110-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd110-120">INPUTS</span></span>

### <span data-ttu-id="fd110-121">System.String</span><span class="sxs-lookup"><span data-stu-id="fd110-121">System.String</span></span>

## <span data-ttu-id="fd110-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd110-122">OUTPUTS</span></span>

### <span data-ttu-id="fd110-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd110-123">System.Boolean</span></span>

## <span data-ttu-id="fd110-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd110-124">NOTES</span></span>

## <span data-ttu-id="fd110-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd110-125">RELATED LINKS</span></span>

[<span data-ttu-id="fd110-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fd110-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fd110-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fd110-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fd110-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fd110-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


