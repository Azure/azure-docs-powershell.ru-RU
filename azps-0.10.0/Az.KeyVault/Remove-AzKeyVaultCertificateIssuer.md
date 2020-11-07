---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910284"
---
# <span data-ttu-id="3c48e-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c48e-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3c48e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c48e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c48e-103">Удаление поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3c48e-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="3c48e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c48e-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c48e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c48e-105">DESCRIPTION</span></span>
<span data-ttu-id="3c48e-106">Командлет **Remove-AzKeyVaultCertificateIssuer** Удаляет поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3c48e-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="3c48e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c48e-107">EXAMPLES</span></span>

### <span data-ttu-id="3c48e-108">Пример 1: Удаление поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="3c48e-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="3c48e-109">Эта команда удаляет издателя сертификата с именем TestIssuer01 из хранилища ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="3c48e-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="3c48e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c48e-110">PARAMETERS</span></span>

### <span data-ttu-id="3c48e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c48e-111">-DefaultProfile</span></span>
<span data-ttu-id="3c48e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3c48e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c48e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3c48e-113">-Force</span></span>
<span data-ttu-id="3c48e-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c48e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c48e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3c48e-115">-Name</span></span>
<span data-ttu-id="3c48e-116">Указывает имя поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="3c48e-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c48e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c48e-117">-PassThru</span></span>
<span data-ttu-id="3c48e-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3c48e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c48e-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3c48e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c48e-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3c48e-120">-VaultName</span></span>
<span data-ttu-id="3c48e-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3c48e-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c48e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c48e-122">-Confirm</span></span>
<span data-ttu-id="3c48e-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c48e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c48e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c48e-124">-WhatIf</span></span>
<span data-ttu-id="3c48e-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c48e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c48e-126">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c48e-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c48e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c48e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c48e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c48e-128">CommonParameters</span></span>
<span data-ttu-id="3c48e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c48e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c48e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c48e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c48e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c48e-131">INPUTS</span></span>

### <span data-ttu-id="3c48e-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c48e-132">None</span></span>
<span data-ttu-id="3c48e-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3c48e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c48e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c48e-134">OUTPUTS</span></span>

### <span data-ttu-id="3c48e-135">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c48e-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3c48e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c48e-136">NOTES</span></span>

## <span data-ttu-id="3c48e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c48e-137">RELATED LINKS</span></span>

[<span data-ttu-id="3c48e-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c48e-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3c48e-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c48e-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


