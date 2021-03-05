---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 12881d387d1e98bef8ca1fa00790b0332a338b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973384"
---
# <span data-ttu-id="2d09b-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d09b-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="2d09b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d09b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d09b-103">Отключать статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2d09b-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="2d09b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d09b-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d09b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d09b-105">DESCRIPTION</span></span>
<span data-ttu-id="2d09b-106">Для учетной записи хранилища Azure отключен статический **веб-сайт Disable-AzStorageStaticWebsite.**</span><span class="sxs-lookup"><span data-stu-id="2d09b-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="2d09b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d09b-107">EXAMPLES</span></span>

### <span data-ttu-id="2d09b-108">Пример 1. Отключение статического веб-сайта для учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="2d09b-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="2d09b-109">Эта команда отключает статический веб-сайт для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2d09b-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="2d09b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d09b-110">PARAMETERS</span></span>

### <span data-ttu-id="2d09b-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="2d09b-111">-Context</span></span>
<span data-ttu-id="2d09b-112">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="2d09b-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2d09b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d09b-113">-DefaultProfile</span></span>
<span data-ttu-id="2d09b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d09b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d09b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d09b-115">-PassThru</span></span>
<span data-ttu-id="2d09b-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2d09b-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2d09b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d09b-117">-Confirm</span></span>
<span data-ttu-id="2d09b-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2d09b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d09b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d09b-119">-WhatIf</span></span>
<span data-ttu-id="2d09b-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d09b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d09b-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2d09b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d09b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d09b-122">CommonParameters</span></span>
<span data-ttu-id="2d09b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d09b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d09b-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d09b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d09b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d09b-125">INPUTS</span></span>

### <span data-ttu-id="2d09b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d09b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2d09b-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d09b-127">OUTPUTS</span></span>

### <span data-ttu-id="2d09b-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="2d09b-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="2d09b-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d09b-129">NOTES</span></span>

## <span data-ttu-id="2d09b-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d09b-130">RELATED LINKS</span></span>
