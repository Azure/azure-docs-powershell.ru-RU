---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411500"
---
# <span data-ttu-id="103bc-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="103bc-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="103bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="103bc-102">SYNOPSIS</span></span>
<span data-ttu-id="103bc-103">Удаляет приложение из учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="103bc-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="103bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="103bc-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="103bc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="103bc-105">DESCRIPTION</span></span>
<span data-ttu-id="103bc-106">С **его использованием** можно удалить приложение из учетной записи Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="103bc-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="103bc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="103bc-107">EXAMPLES</span></span>

### <span data-ttu-id="103bc-108">Пример 1. Удаление приложения из учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="103bc-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="103bc-109">Эта команда удаляет приложение Litware из учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="103bc-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="103bc-110">Команда не справилась, если приложение содержит какие-либо пакеты.</span><span class="sxs-lookup"><span data-stu-id="103bc-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="103bc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="103bc-111">PARAMETERS</span></span>

### <span data-ttu-id="103bc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="103bc-112">-AccountName</span></span>
<span data-ttu-id="103bc-113">Имя учетной записи пакета, из которой этот cmdlet удаляет приложение.</span><span class="sxs-lookup"><span data-stu-id="103bc-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="103bc-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="103bc-114">-ApplicationName</span></span>
<span data-ttu-id="103bc-115">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="103bc-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103bc-116">-DefaultProfile</span></span>
<span data-ttu-id="103bc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="103bc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="103bc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="103bc-118">-ResourceGroupName</span></span>
<span data-ttu-id="103bc-119">Имя группы ресурсов, которая содержит учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="103bc-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="103bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103bc-120">CommonParameters</span></span>
<span data-ttu-id="103bc-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103bc-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="103bc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103bc-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="103bc-123">INPUTS</span></span>

### <span data-ttu-id="103bc-124">System.String</span><span class="sxs-lookup"><span data-stu-id="103bc-124">System.String</span></span>

## <span data-ttu-id="103bc-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="103bc-125">OUTPUTS</span></span>

### <span data-ttu-id="103bc-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="103bc-126">System.Void</span></span>

## <span data-ttu-id="103bc-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="103bc-127">NOTES</span></span>

## <span data-ttu-id="103bc-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="103bc-128">RELATED LINKS</span></span>

[<span data-ttu-id="103bc-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="103bc-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="103bc-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="103bc-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="103bc-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="103bc-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="103bc-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="103bc-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="103bc-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="103bc-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="103bc-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="103bc-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


