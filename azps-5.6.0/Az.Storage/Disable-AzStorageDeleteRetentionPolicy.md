---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: dac884a0faf44380f19447f2d52af1e172feb9a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973395"
---
# <span data-ttu-id="99bcd-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="99bcd-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="99bcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="99bcd-103">Отключите политику хранения удаления для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="99bcd-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="99bcd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99bcd-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99bcd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="99bcd-106">Cmdlet **Disable-AzStorageDeleteRetentionPolicy** отключает политику хранения удаления для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="99bcd-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="99bcd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99bcd-107">EXAMPLES</span></span>

### <span data-ttu-id="99bcd-108">Пример 1. Отключение политики хранения удаления для службы BLOB-документов</span><span class="sxs-lookup"><span data-stu-id="99bcd-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="99bcd-109">Эта команда отключает политику хранения удаления для службы BLOB-документов.</span><span class="sxs-lookup"><span data-stu-id="99bcd-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="99bcd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99bcd-110">PARAMETERS</span></span>

### <span data-ttu-id="99bcd-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="99bcd-111">-Context</span></span>
<span data-ttu-id="99bcd-112">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="99bcd-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="99bcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99bcd-113">-DefaultProfile</span></span>
<span data-ttu-id="99bcd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99bcd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99bcd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99bcd-115">-PassThru</span></span>
<span data-ttu-id="99bcd-116">Отображение свойств DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="99bcd-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="99bcd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99bcd-117">-Confirm</span></span>
<span data-ttu-id="99bcd-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="99bcd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99bcd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99bcd-119">-WhatIf</span></span>
<span data-ttu-id="99bcd-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99bcd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99bcd-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="99bcd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99bcd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bcd-122">CommonParameters</span></span>
<span data-ttu-id="99bcd-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99bcd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bcd-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99bcd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bcd-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99bcd-125">INPUTS</span></span>

### <span data-ttu-id="99bcd-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="99bcd-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="99bcd-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99bcd-127">OUTPUTS</span></span>

### <span data-ttu-id="99bcd-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="99bcd-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="99bcd-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99bcd-129">NOTES</span></span>

## <span data-ttu-id="99bcd-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99bcd-130">RELATED LINKS</span></span>
