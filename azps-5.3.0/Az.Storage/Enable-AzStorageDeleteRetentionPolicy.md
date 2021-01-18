---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505853"
---
# <span data-ttu-id="be17c-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="be17c-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="be17c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be17c-102">SYNOPSIS</span></span>
<span data-ttu-id="be17c-103">Включить политику хранения для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="be17c-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="be17c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be17c-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be17c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be17c-105">DESCRIPTION</span></span>
<span data-ttu-id="be17c-106">С **помощью cmdlet Enable-AzStorageDeleteRetentionPolicy** можно удалить политику хранения для службы BLOB-хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="be17c-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="be17c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be17c-107">EXAMPLES</span></span>

### <span data-ttu-id="be17c-108">Пример 1. Включить политику хранения для службы BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="be17c-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="be17c-109">Эта команда позволяет удалить политику хранения для службы BLOB-документов и установить для удаленных дней хранения BLOB-3.</span><span class="sxs-lookup"><span data-stu-id="be17c-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="be17c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be17c-110">PARAMETERS</span></span>

### <span data-ttu-id="be17c-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="be17c-111">-Context</span></span>
<span data-ttu-id="be17c-112">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="be17c-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be17c-113">-DefaultProfile</span></span>
<span data-ttu-id="be17c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be17c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be17c-115">-PassThru</span></span>
<span data-ttu-id="be17c-116">Отображение свойств DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="be17c-116">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="be17c-117">-RetentionDays</span></span>
<span data-ttu-id="be17c-118">Определяет количество дней хранения для политики DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="be17c-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be17c-119">-Confirm</span></span>
<span data-ttu-id="be17c-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be17c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be17c-121">-WhatIf</span></span>
<span data-ttu-id="be17c-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be17c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be17c-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="be17c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be17c-124">CommonParameters</span></span>
<span data-ttu-id="be17c-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be17c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be17c-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be17c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be17c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be17c-127">INPUTS</span></span>

### <span data-ttu-id="be17c-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="be17c-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="be17c-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be17c-129">OUTPUTS</span></span>

### <span data-ttu-id="be17c-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="be17c-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="be17c-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be17c-131">NOTES</span></span>

## <span data-ttu-id="be17c-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be17c-132">RELATED LINKS</span></span>
