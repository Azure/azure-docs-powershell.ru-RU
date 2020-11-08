---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064988"
---
# <span data-ttu-id="316e5-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="316e5-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="316e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="316e5-102">SYNOPSIS</span></span>
<span data-ttu-id="316e5-103">Пытается включить шифрование для указанной учетной записи Data Lake Store с помощью пользовательского хранилища ключей, управляемого пользователем.</span><span class="sxs-lookup"><span data-stu-id="316e5-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="316e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="316e5-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="316e5-105">DESCRIPTION</span></span>
<span data-ttu-id="316e5-106">Командлет **Enable-AzDataLakeStoreKeyVault** пытается включить управляемое пользователем хранилище ключей для шифрования указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="316e5-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="316e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="316e5-107">EXAMPLES</span></span>

### <span data-ttu-id="316e5-108">Пример 1: включение хранилища ключей для учетной записи ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="316e5-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="316e5-109">Эта команда пытается включить пользовательское хранилище ключей, управляемое пользователем, для учетной записи Data Lake Store с именем ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="316e5-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="316e5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="316e5-110">PARAMETERS</span></span>

### <span data-ttu-id="316e5-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="316e5-111">-Account</span></span>
<span data-ttu-id="316e5-112">Учетная запись Data Lake Store для включения хранилища ключей, управляемого пользователем, для</span><span class="sxs-lookup"><span data-stu-id="316e5-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="316e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316e5-113">-DefaultProfile</span></span>
<span data-ttu-id="316e5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="316e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="316e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="316e5-116">Имя группы ресурсов, связанной с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="316e5-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="316e5-117">Если не указано, будет предпринята попытка обнаружения.</span><span class="sxs-lookup"><span data-stu-id="316e5-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="316e5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="316e5-118">-Confirm</span></span>
<span data-ttu-id="316e5-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="316e5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316e5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316e5-120">-WhatIf</span></span>
<span data-ttu-id="316e5-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="316e5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="316e5-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="316e5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316e5-123">CommonParameters</span></span>
<span data-ttu-id="316e5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="316e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316e5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316e5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316e5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="316e5-126">INPUTS</span></span>

### <span data-ttu-id="316e5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="316e5-127">System.String</span></span>

## <span data-ttu-id="316e5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="316e5-128">OUTPUTS</span></span>

### <span data-ttu-id="316e5-129">System. void</span><span class="sxs-lookup"><span data-stu-id="316e5-129">System.Void</span></span>

## <span data-ttu-id="316e5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="316e5-130">NOTES</span></span>

## <span data-ttu-id="316e5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="316e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="316e5-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="316e5-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="316e5-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="316e5-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

