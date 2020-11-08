---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066905"
---
# <span data-ttu-id="66747-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66747-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="66747-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66747-102">SYNOPSIS</span></span>
<span data-ttu-id="66747-103">Удаляет приложение из пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="66747-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="66747-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66747-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66747-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66747-105">DESCRIPTION</span></span>
<span data-ttu-id="66747-106">Командлет **Remove-AzBatchApplication** удаляет приложение из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="66747-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="66747-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66747-107">EXAMPLES</span></span>

### <span data-ttu-id="66747-108">Пример 1: Удаление приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="66747-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="66747-109">Эта команда удаляет приложение беседа Litware из учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="66747-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="66747-110">Команда не выполняется, если приложение включает в себя пакеты.</span><span class="sxs-lookup"><span data-stu-id="66747-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="66747-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66747-111">PARAMETERS</span></span>

### <span data-ttu-id="66747-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="66747-112">-AccountName</span></span>
<span data-ttu-id="66747-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет приложение.</span><span class="sxs-lookup"><span data-stu-id="66747-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="66747-114">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="66747-114">-ApplicationName</span></span>
<span data-ttu-id="66747-115">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="66747-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="66747-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66747-116">-DefaultProfile</span></span>
<span data-ttu-id="66747-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66747-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66747-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66747-118">-ResourceGroupName</span></span>
<span data-ttu-id="66747-119">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="66747-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="66747-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66747-120">CommonParameters</span></span>
<span data-ttu-id="66747-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66747-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66747-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66747-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66747-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66747-123">INPUTS</span></span>

### <span data-ttu-id="66747-124">System. String</span><span class="sxs-lookup"><span data-stu-id="66747-124">System.String</span></span>

## <span data-ttu-id="66747-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66747-125">OUTPUTS</span></span>

### <span data-ttu-id="66747-126">System. void</span><span class="sxs-lookup"><span data-stu-id="66747-126">System.Void</span></span>

## <span data-ttu-id="66747-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="66747-127">NOTES</span></span>

## <span data-ttu-id="66747-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66747-128">RELATED LINKS</span></span>

[<span data-ttu-id="66747-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66747-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="66747-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="66747-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="66747-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66747-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="66747-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="66747-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="66747-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="66747-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="66747-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66747-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


