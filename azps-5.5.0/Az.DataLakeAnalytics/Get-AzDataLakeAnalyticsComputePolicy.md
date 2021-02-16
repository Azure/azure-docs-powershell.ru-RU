---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242733"
---
# <span data-ttu-id="edba3-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="edba3-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="edba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edba3-102">SYNOPSIS</span></span>
<span data-ttu-id="edba3-103">Возвращает политику или список политик.</span><span class="sxs-lookup"><span data-stu-id="edba3-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="edba3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="edba3-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edba3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edba3-105">DESCRIPTION</span></span>
<span data-ttu-id="edba3-106">**Get-AzDataLakeAnalyticsComputePolicy** получает указанную политику Azure Data Lake Analytics или список политик.</span><span class="sxs-lookup"><span data-stu-id="edba3-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="edba3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="edba3-107">EXAMPLES</span></span>

### <span data-ttu-id="edba3-108">Пример 1. Получить указанную политику расчета</span><span class="sxs-lookup"><span data-stu-id="edba3-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="edba3-109">Эта команда получает указанную вычислительную политику с именем myPolicy в учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="edba3-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="edba3-110">Пример 2. Получить список всех политик вычисления в учетной записи</span><span class="sxs-lookup"><span data-stu-id="edba3-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="edba3-111">Эта команда получает список всех политик вычислений в учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="edba3-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="edba3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edba3-112">PARAMETERS</span></span>

### <span data-ttu-id="edba3-113">-Account</span><span class="sxs-lookup"><span data-stu-id="edba3-113">-Account</span></span>
<span data-ttu-id="edba3-114">Имя учетной записи, из которого будут получаться вычисляемая политика или политики.</span><span class="sxs-lookup"><span data-stu-id="edba3-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edba3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edba3-115">-DefaultProfile</span></span>
<span data-ttu-id="edba3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="edba3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edba3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="edba3-117">-Name</span></span>
<span data-ttu-id="edba3-118">Имя вычисляемой политики, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="edba3-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edba3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edba3-119">-ResourceGroupName</span></span>
<span data-ttu-id="edba3-120">Имя группы ресурсов, под которой вы и есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="edba3-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="edba3-121">Необязательный и попытается найти, если он не предоставлен.</span><span class="sxs-lookup"><span data-stu-id="edba3-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edba3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edba3-122">CommonParameters</span></span>
<span data-ttu-id="edba3-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edba3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edba3-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edba3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edba3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edba3-125">INPUTS</span></span>

### <span data-ttu-id="edba3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="edba3-126">System.String</span></span>

## <span data-ttu-id="edba3-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edba3-127">OUTPUTS</span></span>

### <span data-ttu-id="edba3-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtaLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="edba3-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="edba3-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="edba3-129">NOTES</span></span>

## <span data-ttu-id="edba3-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edba3-130">RELATED LINKS</span></span>
