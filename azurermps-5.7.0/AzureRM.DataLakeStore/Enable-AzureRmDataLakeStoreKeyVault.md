---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 062df0ddadc3cc0cfb2e1f0ef9954454b08c4352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561836"
---
# <span data-ttu-id="cf71a-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="cf71a-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="cf71a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf71a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf71a-103">Пытается включить шифрование для указанной учетной записи Data Lake Store с помощью пользовательского хранилища ключей, управляемого пользователем.</span><span class="sxs-lookup"><span data-stu-id="cf71a-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf71a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf71a-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf71a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf71a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf71a-106">Командлет **Enable-AzureRmDataLakeStoreKeyVault** пытается включить управляемое пользователем хранилище ключей для шифрования указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cf71a-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="cf71a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf71a-107">EXAMPLES</span></span>

### <span data-ttu-id="cf71a-108">Пример 1: включение хранилища ключей для учетной записи ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="cf71a-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="cf71a-109">Эта команда пытается включить пользовательское хранилище ключей, управляемое пользователем, для учетной записи Data Lake Store с именем ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="cf71a-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="cf71a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf71a-110">PARAMETERS</span></span>

### <span data-ttu-id="cf71a-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="cf71a-111">-Account</span></span>
<span data-ttu-id="cf71a-112">Учетная запись Data Lake Store для включения хранилища ключей, управляемого пользователем, для</span><span class="sxs-lookup"><span data-stu-id="cf71a-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf71a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf71a-113">-DefaultProfile</span></span>
<span data-ttu-id="cf71a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cf71a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf71a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf71a-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf71a-116">Имя группы ресурсов, связанной с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="cf71a-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="cf71a-117">Если не указано, будет предпринята попытка обнаружения.</span><span class="sxs-lookup"><span data-stu-id="cf71a-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf71a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf71a-118">-Confirm</span></span>
<span data-ttu-id="cf71a-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf71a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf71a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf71a-120">-WhatIf</span></span>
<span data-ttu-id="cf71a-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf71a-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf71a-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf71a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf71a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf71a-123">CommonParameters</span></span>
<span data-ttu-id="cf71a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf71a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf71a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf71a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf71a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf71a-126">INPUTS</span></span>

### <span data-ttu-id="cf71a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cf71a-127">System.String</span></span>

## <span data-ttu-id="cf71a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf71a-128">OUTPUTS</span></span>

## <span data-ttu-id="cf71a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf71a-129">NOTES</span></span>

## <span data-ttu-id="cf71a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf71a-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf71a-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="cf71a-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="cf71a-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="cf71a-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

