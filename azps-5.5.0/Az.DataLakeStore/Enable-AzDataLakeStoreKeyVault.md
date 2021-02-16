---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243888"
---
# <span data-ttu-id="718b4-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="718b4-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="718b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="718b4-102">SYNOPSIS</span></span>
<span data-ttu-id="718b4-103">Попытка включить управляемый пользователем key Vault для шифрования указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="718b4-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="718b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="718b4-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="718b4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="718b4-105">DESCRIPTION</span></span>
<span data-ttu-id="718b4-106">С **помощью cmdlet Enable-AzDataLakeStoreKeyVault** можно включить управляемое пользователем хранилище ключей для шифрования указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="718b4-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="718b4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="718b4-107">EXAMPLES</span></span>

### <span data-ttu-id="718b4-108">Пример 1. Включить хранилище ключей для учетной записи ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="718b4-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="718b4-109">Эта команда пытается включить управляемое пользователем хранилище ключей для учетной записи Магазина данных ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="718b4-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="718b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="718b4-110">PARAMETERS</span></span>

### <span data-ttu-id="718b4-111">-Account</span><span class="sxs-lookup"><span data-stu-id="718b4-111">-Account</span></span>
<span data-ttu-id="718b4-112">Учетная запись Data Lake Store для обеспечения управляемого пользователем хранилища ключей для</span><span class="sxs-lookup"><span data-stu-id="718b4-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718b4-113">-DefaultProfile</span></span>
<span data-ttu-id="718b4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="718b4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="718b4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718b4-115">-ResourceGroupName</span></span>
<span data-ttu-id="718b4-116">Имя группы ресурсов, связанной с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="718b4-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="718b4-117">Если он не указан, будет предпринята попытка обнаружения.</span><span class="sxs-lookup"><span data-stu-id="718b4-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="718b4-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="718b4-118">-Confirm</span></span>
<span data-ttu-id="718b4-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="718b4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="718b4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="718b4-120">-WhatIf</span></span>
<span data-ttu-id="718b4-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="718b4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="718b4-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="718b4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="718b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718b4-123">CommonParameters</span></span>
<span data-ttu-id="718b4-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718b4-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718b4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718b4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="718b4-126">INPUTS</span></span>

### <span data-ttu-id="718b4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="718b4-127">System.String</span></span>

## <span data-ttu-id="718b4-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="718b4-128">OUTPUTS</span></span>

### <span data-ttu-id="718b4-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="718b4-129">System.Void</span></span>

## <span data-ttu-id="718b4-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="718b4-130">NOTES</span></span>

## <span data-ttu-id="718b4-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="718b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="718b4-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718b4-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="718b4-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="718b4-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

