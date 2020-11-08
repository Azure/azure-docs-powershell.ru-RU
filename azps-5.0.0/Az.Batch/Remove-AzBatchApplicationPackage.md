---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247073"
---
# <span data-ttu-id="a8443-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a8443-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="a8443-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8443-102">SYNOPSIS</span></span>
<span data-ttu-id="a8443-103">Удаляет запись пакета приложения и двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="a8443-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="a8443-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8443-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8443-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8443-105">DESCRIPTION</span></span>
<span data-ttu-id="a8443-106">Командлет **Remove-AzBatchApplicationPackage** удаляет запись пакета приложения и двоичный файл из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="a8443-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="a8443-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8443-107">EXAMPLES</span></span>

### <span data-ttu-id="a8443-108">Пример 1: Удаление пакета приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="a8443-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="a8443-109">Эта команда удаляет версию 1,0 приложения беседа Litware из учетной записи ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="a8443-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="a8443-110">Команда удаляет запись пакета и большой двоичный объект, который содержит двоичный файл пакета.</span><span class="sxs-lookup"><span data-stu-id="a8443-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="a8443-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8443-111">PARAMETERS</span></span>

### <span data-ttu-id="a8443-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="a8443-112">-AccountName</span></span>
<span data-ttu-id="a8443-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="a8443-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="a8443-114">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="a8443-114">-ApplicationName</span></span>
<span data-ttu-id="a8443-115">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="a8443-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="a8443-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="a8443-116">-ApplicationVersion</span></span>
<span data-ttu-id="a8443-117">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="a8443-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8443-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8443-118">-DefaultProfile</span></span>
<span data-ttu-id="a8443-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8443-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8443-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8443-120">-ResourceGroupName</span></span>
<span data-ttu-id="a8443-121">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="a8443-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a8443-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8443-122">CommonParameters</span></span>
<span data-ttu-id="a8443-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8443-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8443-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8443-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8443-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8443-125">INPUTS</span></span>

### <span data-ttu-id="a8443-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a8443-126">System.String</span></span>

## <span data-ttu-id="a8443-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8443-127">OUTPUTS</span></span>

### <span data-ttu-id="a8443-128">System. void</span><span class="sxs-lookup"><span data-stu-id="a8443-128">System.Void</span></span>

## <span data-ttu-id="a8443-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8443-129">NOTES</span></span>

## <span data-ttu-id="a8443-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8443-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8443-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a8443-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="a8443-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a8443-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="a8443-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a8443-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="a8443-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a8443-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="a8443-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a8443-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="a8443-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a8443-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


