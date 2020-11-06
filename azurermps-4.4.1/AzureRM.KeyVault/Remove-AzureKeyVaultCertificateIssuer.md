---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568063"
---
# <span data-ttu-id="af2a4-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="af2a4-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="af2a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="af2a4-103">Удаление поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="af2a4-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af2a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af2a4-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af2a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af2a4-105">DESCRIPTION</span></span>
<span data-ttu-id="af2a4-106">Командлет **Remove-AzureKeyVaultCertificateIssuer** Удаляет поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="af2a4-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="af2a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af2a4-107">EXAMPLES</span></span>

### <span data-ttu-id="af2a4-108">Пример 1: Удаление поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="af2a4-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="af2a4-109">Эта команда удаляет издателя сертификата с именем TestIssuer01 из хранилища ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="af2a4-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="af2a4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af2a4-110">PARAMETERS</span></span>

### <span data-ttu-id="af2a4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="af2a4-111">-Force</span></span>
<span data-ttu-id="af2a4-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="af2a4-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af2a4-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af2a4-113">-Name</span></span>
<span data-ttu-id="af2a4-114">Указывает имя поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="af2a4-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2a4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af2a4-115">-PassThru</span></span>
<span data-ttu-id="af2a4-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="af2a4-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af2a4-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="af2a4-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af2a4-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="af2a4-118">-VaultName</span></span>
<span data-ttu-id="af2a4-119">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="af2a4-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="af2a4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af2a4-120">-Confirm</span></span>
<span data-ttu-id="af2a4-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af2a4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af2a4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2a4-122">-WhatIf</span></span>
<span data-ttu-id="af2a4-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af2a4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2a4-124">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af2a4-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2a4-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af2a4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af2a4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2a4-126">-DefaultProfile</span></span>
<span data-ttu-id="af2a4-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af2a4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2a4-128">CommonParameters</span></span>
<span data-ttu-id="af2a4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af2a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2a4-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2a4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2a4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af2a4-131">INPUTS</span></span>

## <span data-ttu-id="af2a4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af2a4-132">OUTPUTS</span></span>

### <span data-ttu-id="af2a4-133">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="af2a4-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="af2a4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="af2a4-134">NOTES</span></span>

## <span data-ttu-id="af2a4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af2a4-135">RELATED LINKS</span></span>

[<span data-ttu-id="af2a4-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="af2a4-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="af2a4-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="af2a4-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


