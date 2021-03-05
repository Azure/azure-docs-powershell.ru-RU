---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: 25526e7c83746b67a5272ab94f3d523947795c1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973315"
---
# <span data-ttu-id="52404-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="52404-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="52404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52404-102">SYNOPSIS</span></span>
<span data-ttu-id="52404-103">Включить статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="52404-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="52404-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52404-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52404-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52404-105">DESCRIPTION</span></span>
<span data-ttu-id="52404-106">С **помощью cmdlet Enable-AzStorageStaticWebsite** можно включить статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="52404-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="52404-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52404-107">EXAMPLES</span></span>

### <span data-ttu-id="52404-108">Пример 1. Включить статический веб-сайт для учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="52404-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="52404-109">Эта команда позволяет использовать статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="52404-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="52404-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52404-110">PARAMETERS</span></span>

### <span data-ttu-id="52404-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="52404-111">-Context</span></span>
<span data-ttu-id="52404-112">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="52404-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="52404-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52404-113">-DefaultProfile</span></span>
<span data-ttu-id="52404-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52404-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52404-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="52404-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="52404-116">Путь к документу об ошибке, который должен быть показан при выдаче значения 404 (т. е. когда браузер запрашивает страницу, которая не существует).</span><span class="sxs-lookup"><span data-stu-id="52404-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="52404-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="52404-117">-IndexDocument</span></span>
<span data-ttu-id="52404-118">Имя документа индекса в каждом каталоге.</span><span class="sxs-lookup"><span data-stu-id="52404-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="52404-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52404-119">-PassThru</span></span>
<span data-ttu-id="52404-120">Отображение статического веб-сайта в свойствах службы.</span><span class="sxs-lookup"><span data-stu-id="52404-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="52404-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52404-121">-Confirm</span></span>
<span data-ttu-id="52404-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52404-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52404-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52404-123">-WhatIf</span></span>
<span data-ttu-id="52404-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52404-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52404-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="52404-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52404-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52404-126">CommonParameters</span></span>
<span data-ttu-id="52404-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52404-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52404-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52404-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52404-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52404-129">INPUTS</span></span>

### <span data-ttu-id="52404-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="52404-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="52404-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52404-131">OUTPUTS</span></span>

### <span data-ttu-id="52404-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="52404-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="52404-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52404-133">NOTES</span></span>

## <span data-ttu-id="52404-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52404-134">RELATED LINKS</span></span>
