---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563480"
---
# <span data-ttu-id="1267a-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1267a-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1267a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1267a-102">SYNOPSIS</span></span>
<span data-ttu-id="1267a-103">Удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1267a-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1267a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1267a-104">SYNTAX</span></span>

### <span data-ttu-id="1267a-105">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1267a-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1267a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1267a-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1267a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1267a-107">DESCRIPTION</span></span>
<span data-ttu-id="1267a-108">Командлет **Remove-AzureKeyVaultCertificateOperation** удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1267a-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="1267a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1267a-109">EXAMPLES</span></span>

### <span data-ttu-id="1267a-110">Пример 1: Удаление операции с сертификатом</span><span class="sxs-lookup"><span data-stu-id="1267a-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="1267a-111">Эта команда удаляет операцию с сертификатом с именем TestCert01 из хранилища ключей ContosoKV01 без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1267a-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="1267a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1267a-112">PARAMETERS</span></span>

### <span data-ttu-id="1267a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1267a-113">-DefaultProfile</span></span>
<span data-ttu-id="1267a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1267a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1267a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1267a-115">-Force</span></span>
<span data-ttu-id="1267a-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1267a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1267a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1267a-117">-InputObject</span></span>
<span data-ttu-id="1267a-118">Объект Operation</span><span class="sxs-lookup"><span data-stu-id="1267a-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1267a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1267a-119">-Name</span></span>
<span data-ttu-id="1267a-120">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="1267a-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1267a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1267a-121">-PassThru</span></span>
<span data-ttu-id="1267a-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1267a-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1267a-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1267a-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1267a-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1267a-124">-VaultName</span></span>
<span data-ttu-id="1267a-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1267a-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1267a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1267a-126">-Confirm</span></span>
<span data-ttu-id="1267a-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1267a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1267a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1267a-128">-WhatIf</span></span>
<span data-ttu-id="1267a-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1267a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1267a-130">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1267a-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1267a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1267a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1267a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1267a-132">CommonParameters</span></span>
<span data-ttu-id="1267a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1267a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1267a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1267a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1267a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1267a-135">INPUTS</span></span>

### <span data-ttu-id="1267a-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="1267a-136">None</span></span>
<span data-ttu-id="1267a-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1267a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1267a-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1267a-138">OUTPUTS</span></span>

### <span data-ttu-id="1267a-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1267a-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1267a-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="1267a-140">NOTES</span></span>

## <span data-ttu-id="1267a-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1267a-141">RELATED LINKS</span></span>

[<span data-ttu-id="1267a-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1267a-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="1267a-143">Остановить-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1267a-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

