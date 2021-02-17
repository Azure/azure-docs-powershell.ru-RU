---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232561"
---
# <span data-ttu-id="4576c-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4576c-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="4576c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4576c-102">SYNOPSIS</span></span>
<span data-ttu-id="4576c-103">Включить статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4576c-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="4576c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4576c-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4576c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4576c-105">DESCRIPTION</span></span>
<span data-ttu-id="4576c-106">С **помощью cmdlet Enable-AzStorageStaticWebsite** можно включить статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4576c-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="4576c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4576c-107">EXAMPLES</span></span>

### <span data-ttu-id="4576c-108">Пример 1. Включить статический веб-сайт для учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="4576c-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="4576c-109">Эта команда включает статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4576c-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="4576c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4576c-110">PARAMETERS</span></span>

### <span data-ttu-id="4576c-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4576c-111">-Context</span></span>
<span data-ttu-id="4576c-112">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="4576c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="4576c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4576c-113">-DefaultProfile</span></span>
<span data-ttu-id="4576c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4576c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4576c-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="4576c-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="4576c-116">Путь к документу ошибки, который должен быть показан при выдаче значения 404 (т. е. когда браузер запрашивает страницу, которая не существует).</span><span class="sxs-lookup"><span data-stu-id="4576c-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4576c-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="4576c-117">-IndexDocument</span></span>
<span data-ttu-id="4576c-118">Имя документа индекса в каждом каталоге.</span><span class="sxs-lookup"><span data-stu-id="4576c-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4576c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4576c-119">-PassThru</span></span>
<span data-ttu-id="4576c-120">Отображение статического веб-сайта в свойствах службы.</span><span class="sxs-lookup"><span data-stu-id="4576c-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="4576c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4576c-121">-Confirm</span></span>
<span data-ttu-id="4576c-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4576c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4576c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4576c-123">-WhatIf</span></span>
<span data-ttu-id="4576c-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4576c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4576c-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4576c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4576c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4576c-126">CommonParameters</span></span>
<span data-ttu-id="4576c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4576c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4576c-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4576c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4576c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4576c-129">INPUTS</span></span>

### <span data-ttu-id="4576c-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4576c-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4576c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4576c-131">OUTPUTS</span></span>

### <span data-ttu-id="4576c-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="4576c-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="4576c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4576c-133">NOTES</span></span>

## <span data-ttu-id="4576c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4576c-134">RELATED LINKS</span></span>
