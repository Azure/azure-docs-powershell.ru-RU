---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 88b142943e37009cf21b35bdaadfd209d1d74c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961272"
---
# <span data-ttu-id="1c3e1-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c3e1-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1c3e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3e1-103">Удаляет хранимую политику доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="1c3e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c3e1-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c3e1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3e1-106">**Cmdlet Remove-AzStorageQueueStoredAccessPolicy** удаляет хранимую политику доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="1c3e1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c3e1-107">EXAMPLES</span></span>

### <span data-ttu-id="1c3e1-108">Пример 1. Удаление хранимой политики доступа из очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="1c3e1-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="1c3e1-109">Эта команда удаляет политику доступа с именем Policy04 из очереди хранения MyQueue.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="1c3e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3e1-110">PARAMETERS</span></span>

### <span data-ttu-id="1c3e1-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="1c3e1-111">-Context</span></span>
<span data-ttu-id="1c3e1-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1c3e1-113">Чтобы получить контекст хранилища, воспользуйтесь New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1c3e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3e1-114">-DefaultProfile</span></span>
<span data-ttu-id="1c3e1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3e1-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c3e1-116">-PassThru</span></span>
<span data-ttu-id="1c3e1-117">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1c3e1-118">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1c3e1-119">-Политика</span><span class="sxs-lookup"><span data-stu-id="1c3e1-119">-Policy</span></span>
<span data-ttu-id="1c3e1-120">Указывает имя хранимой политики доступа, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1c3e1-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="1c3e1-121">-Queue</span></span>
<span data-ttu-id="1c3e1-122">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3e1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c3e1-123">-Confirm</span></span>
<span data-ttu-id="1c3e1-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3e1-125">-WhatIf</span></span>
<span data-ttu-id="1c3e1-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3e1-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3e1-128">CommonParameters</span></span>
<span data-ttu-id="1c3e1-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3e1-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3e1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3e1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c3e1-131">INPUTS</span></span>

### <span data-ttu-id="1c3e1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1c3e1-132">System.String</span></span>

### <span data-ttu-id="1c3e1-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c3e1-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1c3e1-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c3e1-134">OUTPUTS</span></span>

### <span data-ttu-id="1c3e1-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c3e1-135">System.Boolean</span></span>

## <span data-ttu-id="1c3e1-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c3e1-136">NOTES</span></span>

## <span data-ttu-id="1c3e1-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c3e1-137">RELATED LINKS</span></span>

[<span data-ttu-id="1c3e1-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c3e1-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1c3e1-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c3e1-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1c3e1-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c3e1-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1c3e1-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c3e1-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
