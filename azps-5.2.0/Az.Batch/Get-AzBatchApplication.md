---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399596"
---
# <span data-ttu-id="f39be-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f39be-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="f39be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f39be-102">SYNOPSIS</span></span>
<span data-ttu-id="f39be-103">Получает сведения об указанном приложении.</span><span class="sxs-lookup"><span data-stu-id="f39be-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="f39be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f39be-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f39be-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39be-105">DESCRIPTION</span></span>
<span data-ttu-id="f39be-106">Чтобы получить сведения о приложении в учетной записи Azure Batch, можно получить сведения о нем с использованием **cmdlet Get-AzBatchApplication.**</span><span class="sxs-lookup"><span data-stu-id="f39be-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="f39be-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f39be-107">EXAMPLES</span></span>

### <span data-ttu-id="f39be-108">Пример 1. Отображение приложений в учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="f39be-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="f39be-109">Эта команда отображает все приложения в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="f39be-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="f39be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f39be-110">PARAMETERS</span></span>

### <span data-ttu-id="f39be-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f39be-111">-AccountName</span></span>
<span data-ttu-id="f39be-112">Имя учетной записи пакета, которая содержит приложение.</span><span class="sxs-lookup"><span data-stu-id="f39be-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="f39be-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f39be-113">-ApplicationName</span></span>
<span data-ttu-id="f39be-114">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="f39be-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f39be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39be-115">-DefaultProfile</span></span>
<span data-ttu-id="f39be-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f39be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f39be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39be-117">-ResourceGroupName</span></span>
<span data-ttu-id="f39be-118">Имя группы ресурсов, которая содержит учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="f39be-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f39be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39be-119">CommonParameters</span></span>
<span data-ttu-id="f39be-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39be-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f39be-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39be-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f39be-122">INPUTS</span></span>

### <span data-ttu-id="f39be-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f39be-123">System.String</span></span>

## <span data-ttu-id="f39be-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f39be-124">OUTPUTS</span></span>

### <span data-ttu-id="f39be-125">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="f39be-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="f39be-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f39be-126">NOTES</span></span>

## <span data-ttu-id="f39be-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f39be-127">RELATED LINKS</span></span>

[<span data-ttu-id="f39be-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f39be-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="f39be-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f39be-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="f39be-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f39be-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="f39be-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f39be-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="f39be-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f39be-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="f39be-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f39be-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


