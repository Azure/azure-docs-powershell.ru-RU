---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403383"
---
# <span data-ttu-id="66bc1-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="66bc1-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="66bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="66bc1-103">Отозову все ключи делегирования пользователей для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="66bc1-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="66bc1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="66bc1-104">SYNTAX</span></span>

### <span data-ttu-id="66bc1-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66bc1-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66bc1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="66bc1-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66bc1-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="66bc1-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66bc1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66bc1-108">DESCRIPTION</span></span>
<span data-ttu-id="66bc1-109">Cmdlet **Revoke-AzStorageAccountUserDelegationKeys** отменяет все ключи делегирования пользователей учетной записи хранения, поэтому все маркеры SAS удостоверений учетной записи хранения также будут отозваны.</span><span class="sxs-lookup"><span data-stu-id="66bc1-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="66bc1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="66bc1-110">EXAMPLES</span></span>

### <span data-ttu-id="66bc1-111">Пример 1. Ото имя всех ключей делегирования пользователей учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="66bc1-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="66bc1-112">В этом примере все ключи делегирования пользователей учетной записи хранения отозваны, поэтому все маркеры SAS удостоверений, созданные на их примере, также будут отозваны.</span><span class="sxs-lookup"><span data-stu-id="66bc1-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="66bc1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66bc1-113">PARAMETERS</span></span>

### <span data-ttu-id="66bc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bc1-114">-DefaultProfile</span></span>
<span data-ttu-id="66bc1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66bc1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66bc1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66bc1-116">-InputObject</span></span>
<span data-ttu-id="66bc1-117">Объект учетной записи хранения, возвращенный Get_AzStorageAccount New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="66bc1-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66bc1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66bc1-118">-PassThru</span></span>
<span data-ttu-id="66bc1-119">Как правило, этот $true возвращает результат успешного завершения, но этот параметр заставляет его возвращать значение ($true).</span><span class="sxs-lookup"><span data-stu-id="66bc1-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="66bc1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66bc1-120">-ResourceGroupName</span></span>
<span data-ttu-id="66bc1-121">Имя группы ресурсов, содержащей ресурс учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="66bc1-121">The resource group name containing the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bc1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66bc1-122">-ResourceId</span></span>
<span data-ttu-id="66bc1-123">ИД ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="66bc1-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66bc1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="66bc1-124">-StorageAccountName</span></span>
<span data-ttu-id="66bc1-125">Имя ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="66bc1-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bc1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66bc1-126">-Confirm</span></span>
<span data-ttu-id="66bc1-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66bc1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bc1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bc1-128">-WhatIf</span></span>
<span data-ttu-id="66bc1-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66bc1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66bc1-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="66bc1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bc1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bc1-131">CommonParameters</span></span>
<span data-ttu-id="66bc1-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66bc1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bc1-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bc1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bc1-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66bc1-134">INPUTS</span></span>

### <span data-ttu-id="66bc1-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66bc1-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="66bc1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="66bc1-136">System.String</span></span>

## <span data-ttu-id="66bc1-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66bc1-137">OUTPUTS</span></span>

### <span data-ttu-id="66bc1-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66bc1-138">System.Boolean</span></span>

## <span data-ttu-id="66bc1-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="66bc1-139">NOTES</span></span>

## <span data-ttu-id="66bc1-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66bc1-140">RELATED LINKS</span></span>
